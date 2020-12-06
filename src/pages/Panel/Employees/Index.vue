<template>
    <section id="tables">
        <mdb-row>
            <mdb-col md="12">
                <mdb-card cascade narrow class="mt-5">
                    <mdb-card-body>
                        <mdb-tbl>
                            <thead class="mdb-color darken-3">
                            <tr class="text-white">
                                <th>#</th>
                                <th>Username</th>
                                <th>FirstName & LastName</th>
                                <th>Mobile</th>
                                <th>Gender</th>
                                <th>Status</th>
                                <th>Action</th>
                            </tr>
                            </thead>
                            <tbody>
                            <tr v-for="(employee, index) in employees.data" :key="employee.id">
                                <td v-text="index+1"></td>
                                <td v-text="employee.username"></td>
                                <td v-text="employee.first_name + ' ' + employee.last_name"></td>
                                <td v-if="employee.gender === 1">Male</td>
                                <td v-if="employee.gender === 0">Famale</td>
                                <td v-text="employee.mobile"></td>
                                <td v-if="employee.status === 'ACTIVE' ">
                                    <p class="btn-sm btn-success disabled text-center">ACTIVE</p>
                                </td>
                                <td v-if="employee.status === 'INACTIVE' ">
                                    <p class="btn-sm btn-dark disabled text-center">INACTIVE</p>
                                </td>
                                <td v-if="employee.status === 'PENDING' ">
                                    <p class="btn-sm btn-warning disabled text-center">PENDING</p>
                                </td>
                                <td v-if="employee.status === 'SUSPENDED' ">
                                    <p class="btn-sm btn-danger disabled text-center">SUSPENDED</p>
                                </td>
                                <td>
                                    <a href="#"
                                       class="text-success text-center" data-toggle="modal"
                                       data-target="#employee-show">
                                        <mdb-icon icon="eye" /></a>

                                    /
                                    <a href="#" data-id="employee.id"
                                       class="text-primary text-center"><mdb-icon icon="pen" /></a>
                                    /
                                    <a href="#"
                                       class="text-danger"><mdb-icon icon="trash" /></a>
                                </td>
                            </tr>
                            </tbody>
                        </mdb-tbl>
                        <pagination :data="employees" @pagination-change-page="getResults"></pagination>
                    </mdb-card-body>
                </mdb-card>
            </mdb-col>
        </mdb-row>
    </section>
</template>

<script>
    import { mdbRow, mdbCol, mdbCard, mdbCardBody, mdbTbl, mdbIcon} from 'mdbvue'
    import {BASE_URL} from '../../../Config.js';
    import axios from 'axios';
    import Swal from 'sweetalert2';
    window.Swal = Swal;
    import Vue from 'vue';

    Vue.component('pagination', require('laravel-vue-pagination'));

    export default {
        name: 'Index',
        components: {
            mdbRow,
            mdbCol,
            mdbCard,
            mdbCardBody,
            mdbTbl,
            mdbIcon
        },
        data () {
            return {
                employees: [{}],
            }
        },
        methods: {
            getResults(page = 1) {
                axios.get(BASE_URL + `/panel/employee/?page=` + page)
                    .then(res => {
                        this.employees = res.data.data;
                    }).catch(() => {
                    Swal.fire(
                        'Warning!',
                        'Service is Unavailable.',
                        'warning',
                    )
                });
            },
        },
        mounted() {
            this.getResults();
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .card.card-cascade .view.gradient-card-header {
        padding: 1rem 1rem;
        text-align: center;
    }
    .card.card-cascade h3,
    .card.card-cascade h4 {
        margin-bottom: 0;
    }
</style>
