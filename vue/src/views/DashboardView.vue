<template>
    <div class="main_content_iner">
        <div class="container-fluid p-0">
            <div class="row justify-content-center">
                <div class="col-lg-12">
                    <div class="single_element">
                        <div class="quick_activity">
                            <div class="row">
                                <div class="col-12">
                                    <div class="quick_activity_wrap">
                                        <div class="single_quick_activity d-flex">
                                            <div class="icon">
                                                <img src="/img/icon/man.svg" alt="image" />
                                            </div>
                                            <div class="count_content">
                                                <h3><span class="counter">{{totalCustomer}}</span></h3>
                                                <p>Total Customer</p>
                                            </div>
                                        </div>
                                        <div class="single_quick_activity d-flex">
                                            <div class="icon">
                                                <img src="/img/icon/cap.svg" alt="image" />
                                            </div>
                                            <div class="count_content">
                                                <h3><span class="counter">{{ Withdrawal }}</span></h3>
                                                <p>Total Withdraw</p>
                                            </div>
                                        </div>
                                        <div class="single_quick_activity d-flex">
                                            <div class="icon">
                                                <img src="/img/icon/wheel.svg" alt="image" />
                                            </div>
                                            <div class="count_content">
                                                <h3><span class="counter">{{Loan}}</span></h3>
                                                <p>Total Lone</p>
                                            </div>
                                        </div>
                                        <div class="single_quick_activity d-flex">
                                            <div class="icon">
                                                <img src="/img/icon/pharma.svg" alt="image" />
                                            </div>
                                            <div class="count_content">
                                                <h3><span class="counter">{{ Payment }}</span></h3>
                                                <p>Total Payment</p>
                                            </div>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-lg-12 col-xl-12">
                    <div class="white_box mb_30">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Bank Survey</h3>
                            </div>
                        </div>
                        <div class="income_servay">
                            <div class="row">
                                <div class="col-md-3">
                                    <div class="count_content">
                                        <h3>$ <span class="counter">{{ todaysWithdrawal }}</span></h3>
                                        <p>Today's Withdraw</p>
                                    </div>
                                </div>
                                <div class="col-md-3">
                                    <div class="count_content">
                                        <h3>$ <span class="counter">{{ todaysPayment }}</span></h3>
                                        <p>Today's Payment</p>
                                    </div>
                                </div>
                                <div class="col-md-3">
                                    <div class="count_content">
                                        <h3>$ <span class="counter">{{ todaysLoan }}</span></h3>
                                        <p>Today's Loan</p>
                                    </div>
                                </div>
                                <div class="col-md-3">
                                    <div class="count_content">
                                        <h3>$ <span class="counter">{{ todaysCashDeposit }}</span></h3>
                                        <p>Today's Cash Diposit</p>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div id="bar_wev"></div>
                    </div>
                </div>
                <div class="col-xl-7">
                    <div class="white_box QA_section card_height_100">
                        <div class="white_box_tittle list_header m-0 align-items-center">
                            <div class="main-title mb-sm-15">
                                <h3 class="m-0 nowrap">Accounts</h3>
                            </div>
                            <div class="box_right d-flex lms_block">
                                <div class="serach_field-area2">
                                    <div class="search_inner">
                                        <form Active="#">
                                            <div class="search_field">
                                                <input type="text" placeholder="Search here..." />
                                            </div>
                                            <button type="submit">
                                                <i class="ti-search"></i>
                                            </button>
                                        </form>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="QA_table">
                            <table class="table lms_table_active2">
                                <thead>
                                    <tr>
                                        <th scope="col">Customer Name</th>
                                        <th scope="col">department</th>
                                        <th scope="col">Appointment Date</th>
                                        <th scope="col">Serial Number</th>
                                        <th scope="col">Amount</th>
                                    </tr>
                                </thead>
                                <tbody>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/pataint.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/2.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/3.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/4.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/5.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/6.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                    <tr>
                                        <th scope="row">
                                            <div class="patient_thumb d-flex align-items-center">
                                                <div class="student_list_img mr_20">
                                                    <img src="/img/patient/6.png" alt="image" />
                                                </div>
                                                <p>Jhon Kural</p>
                                            </div>
                                        </th>
                                        <td>Monte Carlo</td>
                                        <td>11/03/2020</td>
                                        <td>MDC65454</td>
                                        <td>
                                            <div class="amoutn_action d-flex align-items-center">
                                                $29,192
                                                <div class="dropdown ms-4">
                                                    <a class="dropdown-toggle hide_pils" href="#" role="button"
                                                        id="dropdownMenuLink" data-bs-toggle="dropdown"
                                                        aria-haspopup="true" aria-expanded="false">
                                                        <i class="fas fa-ellipsis-v"></i>
                                                    </a>
                                                    <div class="dropdown-menu dropdown-menu-right"
                                                        aria-labelledby="dropdownMenuLink">
                                                        <a class="dropdown-item" href="#">View</a>
                                                        <a class="dropdown-item" href="#">Edit</a>
                                                        <a class="dropdown-item" href="#">Delete</a>
                                                    </div>
                                                </div>
                                            </div>
                                        </td>
                                    </tr>
                                </tbody>
                            </table>
                        </div>
                    </div>
                </div>
                <div class="col-xl-5">
                    <div class="white_box card_height_50 mb_30">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Total Recover Report</h3>
                            </div>
                        </div>
                        <div id="chart-7"></div>
                        <div class="row text-center mt-3">
                            <div class="col-sm-6">
                                <h6 class="heading_6 d-block">Last Month</h6>
                                <p class="m-0">358</p>
                            </div>
                            <div class="col-sm-6">
                                <h6 class="heading_6 d-block">Current Month</h6>
                                <p class="m-0">194</p>
                            </div>
                        </div>
                    </div>
                    <div class="white_box card_height_50 mb_30">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Total Death Report</h3>
                            </div>
                        </div>
                        <div id="chart-8"></div>
                        <div class="row text-center mt-3">
                            <div class="col-sm-6">
                                <h6 class="heading_6 d-block">Last Month</h6>
                                <p class="m-0">358</p>
                            </div>
                            <div class="col-sm-6">
                                <h6 class="heading_6 d-block">Current Month</h6>
                                <p class="m-0">194</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-xl-12">
                    <div class="white_box card_height_100">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Hospital Staff</h3>
                            </div>
                        </div>
                        <div class="staf_list_wrapper sraf_active owl-carousel">
                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/1.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/2.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/3.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/4.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/5.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/1.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/2.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>

                            <div class="single_staf">
                                <div class="staf_thumb">
                                    <img src="/img/staf/3.png" alt="image" />
                                </div>
                                <h4>Dr. Sysla J Smith</h4>
                                <p>Doctor</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-xl-6">
                    <div class="white_box card_height_100">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Recent Activity</h3>
                            </div>
                        </div>
                        <div class="Activity_timeline">
                            <ul>
                                <li>
                                    <div class="activity_bell"></div>
                                    <div class="activity_wrap">
                                        <h6>5 min ago</h6>
                                        <p>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing
                                            elit. Quisque scelerisque
                                        </p>
                                    </div>
                                </li>
                                <li>
                                    <div class="activity_bell"></div>
                                    <div class="activity_wrap">
                                        <h6>5 min ago</h6>
                                        <p>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing
                                            elit. Quisque scelerisque
                                        </p>
                                    </div>
                                </li>
                                <li>
                                    <div class="activity_bell"></div>
                                    <div class="activity_wrap">
                                        <h6>5 min ago</h6>
                                        <p>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing
                                            elit. Quisque scelerisque
                                        </p>
                                    </div>
                                </li>
                                <li>
                                    <div class="activity_bell"></div>
                                    <div class="activity_wrap">
                                        <h6>5 min ago</h6>
                                        <p>
                                            Lorem ipsum dolor sit amet, consectetur adipiscing
                                            elit. Quisque scelerisque
                                        </p>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
                <div class="col-xl-6">
                    <div class="white_box mb_30">
                        <div class="box_header border_bottom_1px">
                            <div class="main-title">
                                <h3 class="mb_25">Recent Activity</h3>
                            </div>
                        </div>
                        <div class="activity_progressbar">
                            <div class="single_progressbar">
                                <h6>USA</h6>
                                <div id="bar1" class="barfiller">
                                    <div class="tipWrap">
                                        <span class="tip"></span>
                                    </div>
                                    <span class="fill" data-percentage="95"></span>
                                </div>
                            </div>
                            <div class="single_progressbar">
                                <h6>AFRICA</h6>
                                <div id="bar2" class="barfiller">
                                    <div class="tipWrap">
                                        <span class="tip"></span>
                                    </div>
                                    <span class="fill" data-percentage="75"></span>
                                </div>
                            </div>
                            <div class="single_progressbar">
                                <h6>UK</h6>
                                <div id="bar3" class="barfiller">
                                    <div class="tipWrap">
                                        <span class="tip"></span>
                                    </div>
                                    <span class="fill" data-percentage="55"></span>
                                </div>
                            </div>
                            <div class="single_progressbar">
                                <h6>CANADA</h6>
                                <div id="bar4" class="barfiller">
                                    <div class="tipWrap">
                                        <span class="tip"></span>
                                    </div>
                                    <span class="fill" data-percentage="25"></span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        totalCustomer: 0,
        totalAmount: 0,
        Calculate:0,
        Withdrawal:0,
        CashDeposit:0,
        Loan:0,
        Payment:0,

        todaysWithdrawal:0,
        todaysCashDeposit:0,
        todaysLoan:0,
        todaysPayment:0,
      };
    },
    mounted() {
      this.fetchTotalAmount();
    },
    methods: {
      fetchTotalAmount() {
        axios.get('http://127.0.0.1:8000/api/calculate')
          .then(res => {
            // console.log('API response:', res.data.data);
            this.Calculate = parseFloat(res.data.data.Calculate);
            this.Withdrawal = parseFloat(res.data.data.Withdrawal);
            this.CashDeposit = parseFloat(res.data.data.CashDeposit);
            this.Loan = parseFloat(res.data.data.Loan);
            this.Payment = parseFloat(res.data.data.Payment);
            this.totalCustomer = parseFloat(res.data.data.Customer);
            this.totalAmount = this.Calculate-this.Withdrawal-this.Loan+this.CashDeposit-this.Payment;

            this.todaysWithdrawal=parseFloat(res.data.data.todaysWithdrawal);
            this.todaysCashDeposit=parseFloat(res.data.data.todaysCashDeposit);
            this.todaysLoan=parseFloat(res.data.data.todaysLoan);
            this.todaysPayment=parseFloat(res.data.data.todaysPayment);
          })
          .catch(error => {
            console.error('Error fetching total amount:', error);
          });
      }
    }
  };
  </script>