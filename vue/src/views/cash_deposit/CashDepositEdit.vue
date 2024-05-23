<script>
import axios from "axios";
import NavbarViewVue from "../inc/NavbarView.vue";

export default {
  components: {
    NavbarViewVue
  },
  data() {
    return {
      url: 'http://127.0.0.1:8000/api/cashDeposit',
      customer_id_list: [],
      customer_id: '',
      amount: '',
      date: '',
      customer_id_listError: '',
      amountError: '',
      dateError: ''
    };
  },
  mounted() {
    this.getCashDeposit();
    this.getCash();
  },
  methods: {
    getCashDeposit() {
      axios.get('http://127.0.0.1:8000/api/customer').then(res => {
        this.customer_id_list = res.data.data;
        })
    },
    getCash() {
      const id = this.$route.params.id;
      axios.get(`${this.url}/${id}/edit`).then((res) => {
        const dt = res.data.data;
        console.log(dt);
        this.customer_id = dt.customer_id;
        this.amount = dt.amount;
        this.date = dt.date;
      }).catch(error => {
        console.error('Error fetching cashDeposit data:', error);
      });

    },
    // validateForm() {
    //   this.customer_idError = this.customer_id ? '' : 'Customer is required.';
    //   this.amountError = this.amount ? '' : 'Amount is required.';
    //   this.dateError = this.date ? '' : 'Date is required.';

    //   return !this.customer_idError && !this.amountError && !this.dateError;
    // },
    updateCashDeposit() {
      // if (this.validateForm()) {
        const id = this.$route.params.id;
        const data = {
          customer_id: this.customer_id,
          amount: this.amount,
          date: this.date
          
        };
        console.log(data);

        axios.put(`${this.url}/${id}`, data).then(res => {
          this.$router.push({ name: 'cashDeposit' });
        }).catch(error => {
        console.error('Error updating cash deposit:', error);
          });
      },
      handleSubmit() {
      this.updateCashDeposit();
      }
    }
      
  }
// }
</script>

<template>
  <main>
    <NavbarViewVue />
    <div class="container card mt-5 ms-2">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="card-header mt-5">
            <h4 class="table_heading">Cash Deposit Edit</h4>
          </div>
          <div class="card-body">
            <form @submit.prevent="handleSubmit">
              <div class="mb-3">
                <label for="customerid" class="form-label">Customer Name</label>
                <select
                  class="form-select"
                  v-model="customer_id"
                  aria-label="Default select example"
                >
                  <option disabled value="">Select customer name</option>
                  <option v-for="(p, i) in customer_id_list" :key="i" :value="p.id">
                    {{ p.customer_name }}
                  </option>
                </select>
                <p style="color: red" v-if="customer_id_listError">
                  {{ customer_id_listError }}
                </p>
              </div>

              <div class="mb-3">
                <label for="cashDeposit" class="form-label">Cash Deposit Amount</label>
                <input
                  type="number"
                  v-model="amount"
                  class="form-control"
                  id="cashDeposit"
                  placeholder="Enter cash Deposit amount"
                />
                <p style="color: red" v-if="amountError">
                  {{ amountError }}
                </p>
              </div>

              <div class="mb-3">
                <label for="date" class="form-label">Date</label>
                <input type="date" v-model="date" class="form-control" id="date" placeholder="Enter date">
                <p style="color:red" v-if="dateError">
                  {{ dateError }}
                </p>
              </div>

              <button type="submit" class="btn btn-primary">Submit</button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
