<template>
    <!-- Sidebar -->
    <div class="sidebar-fixed position-fixed">
        <a class="logo-wrapper"
        ><img alt="" class="img-fluid" src="../../../src/assets/logo-mdb-vue-small.png"
        /></a>
        <mdb-list-group class="list-group-flush">
            <!--//-->
            <router-link to="/dashboard" @click.native="activeItem = 1">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 1 && 'active'"
                ><mdb-icon
                        icon="chart-pie"
                        class="mr-3"
                />Dashboard</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/profile" @click.native="activeItem = 2">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 2 && 'active'"
                ><mdb-icon icon="user" class="mr-3" />Profile</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/tables" @click.native="activeItem = 3">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 3 && 'active'"
                ><mdb-icon icon="table" class="mr-3" />Tables</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/maps" @click.native="activeItem = 4">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 4 && 'active'"
                ><mdb-icon icon="map" class="mr-3" />Maps</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/404" @click.native="activeItem = 5">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 5 && 'active'"
                ><mdb-icon
                        icon="exclamation"
                        class="mr-3"
                />404</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/employees" @click.native="activeItem = 2">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 2 && 'active'"
                ><mdb-icon icon="user" class="mr-3" />Employees</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/tables" @click.native="activeItem = 3">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 3 && 'active'"
                ><mdb-icon icon="table" class="mr-3" />Users</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/profile" @click.native="activeItem = 2">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 2 && 'active'"
                ><mdb-icon icon="user" class="mr-3" />Categories</mdb-list-group-item
                >
            </router-link>
            <!--//-->
            <router-link to="/tables" @click.native="activeItem = 3">
                <mdb-list-group-item
                        :action="true"
                        :class="activeItem === 3 && 'active'"
                ><mdb-icon icon="table" class="mr-3" />Products</mdb-list-group-item
                >
            </router-link>
            <!--//-->
        </mdb-list-group>
    </div>
    <!-- /Sidebar  -->
</template>

<script>
    import {
        mdbIcon,
        mdbListGroup,
        mdbListGroupItem,
    } from "mdbvue";

    export default {
        name: "Sidebar",
        components: {
            mdbListGroup,
            mdbListGroupItem,
            mdbIcon,
        },
    }
</script>

<style scoped>

</style>