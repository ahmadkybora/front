<template>
    <!--Navbar-->
    <mdb-navbar class="flexible-navbar white" light position="top" scrolling>
        <mdb-navbar-brand href="https://mdbootstrap.com/docs/vue/" target="_blank"
        >MDB</mdb-navbar-brand
        >
        <mdb-navbar-toggler>
            <mdb-navbar-nav left>
                <mdb-nav-item to="/" waves-fixed active class="active"
                >Home</mdb-nav-item
                >
                <mdb-nav-item
                        href="https://mdbootstrap.com/docs/vue/getting-started/quick-start/"
                        waves-fixed
                >About MDB</mdb-nav-item
                >
                <mdb-nav-item
                        href="https://mdbootstrap.com/docs/vue/getting-started/download/"
                        waves-fixed
                >Free download</mdb-nav-item
                >
                <mdb-nav-item
                        href="https://mdbootstrap.com/education/bootstrap/"
                        waves-fixed
                >Free tutorials</mdb-nav-item
                >
            </mdb-navbar-nav>
            <mdb-navbar-nav right>
                <mdb-nav-item href="#!" waves-fixed
                ><mdb-icon fab class="text-black" icon="facebook-square"
                /></mdb-nav-item>
                <mdb-nav-item href="#!" waves-fixed
                ><mdb-icon fab icon="twitter"
                /></mdb-nav-item>
                <mdb-nav-item
                        href="https://github.com/mdbootstrap/bootstrap-material-design"
                        waves-fixed
                        class="border border-light rounded mr-1"
                        target="_blank"
                ><mdb-icon fab icon="github" class="mr-2" />MDB GitHub
                </mdb-nav-item>
                <mdb-nav-item
                        href="https://mdbootstrap.com/products/vue-ui-kit/"
                        waves-fixed
                        class="border border-light rounded"
                        target="_blank"
                ><mdb-icon icon="gem" far class="mr-2" />Go Pro
                </mdb-nav-item>
            </mdb-navbar-nav>
        </mdb-navbar-toggler>
    </mdb-navbar>
    <!--/.Navbar-->
</template>

<script>
    import {
        mdbNavbar,
        mdbNavbarBrand,
        mdbNavItem,
        mdbNavbarNav,
        mdbNavbarToggler,
        mdbIcon,
    } from "mdbvue";

    export default {
        name: "Navbar",
        components: {
            mdbNavbar,
            mdbNavbarBrand,
            mdbNavItem,
            mdbNavbarNav,
            mdbNavbarToggler,
            mdbIcon,
        }
    }
</script>

<style scoped>

</style>