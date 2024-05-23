<script>
import NavbarViewVue from '../inc/NavbarView.vue'
import axios from 'axios'

export default {
  components: {
    NavbarViewVue
  },
  data() {
    return {
      url: 'http://127.0.0.1:8000/api/withdrawal',
      customer_id_list: [],
      customer_id: '',
      deposit_amount: '',
      date: '',
      customer_id_listError: '',
      deposit_amountError: '',
      dateError: ''
    }
  },
  mounted() {
    this.getWithdrawal();
    this.getCustomer();
  },
  methods: {
    getCustomer() {
      axios.get('http://127.0.0.1:8000/api/customer').then((res) => {
        this.customer_id_list = res.data.data
      })
    },
    getWithdrawal() {
      const id = this.$route.params.id;
      axios.get(`${this.url}/${id}/edit`).then((res) => {
        const dt = res.data.data;
        this.customer_id = dt.customer_id;
        this.deposit_amount = dt.deposit_amount;
        this.date = dt.date;
      }).catch(error => {
        console.error('Error fetching withdrawal data:', error);
      });
    },
    updateWithdrawal() {
      const id = this.$route.params.id;
      const data = {
        customer_id: this.customer_id,
        deposit_amount: this.deposit_amount,
        date: this.date
      };
      axios.put(`${this.url}/${id}`, data).then(res => {
        this.$router.push({ name: 'withdrawal' });
      }).catch(error => {
        console.error('Error updating withdrawal:', error);
      });
    },
    handleSubmit() {
      this.updateWithdrawal();
    }
  }
}
</script>

<template>
  <main>
    <NavbarViewVue />
    <div class="container card mt-5 ms-2">
      <div class="row justify-content-center">
        <div class="col-md-6">
          <div class="card-header mt-5">Withdrawal Edit</div>
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
                <label for="withdrawal" class="form-label">Withdrawal Amount</label>
                <input
                  type="number"
                  v-model="deposit_amount"
                  class="form-control"
                  id="withdrawal"
                  placeholder="Enter withdrawal amount"
                />
                <p style="color: red" v-if="deposit_amountError">
                  {{ deposit_amountError }}
                </p>
              </div>

              <div class="mb-3">
                <label for="date" class="form-label">Date</label>
                <input
                  type="date"
                  v-model="date"
                  class="form-control"
                  id="date"
                  placeholder="Enter Your date"
                />
                <p style="color: red" v-if="dateError">
                  {{ dateError }}
                </p>
              </div>

              <button type="submit" class="btn btn-primary">
                Submit
              </button>
            </form>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>
