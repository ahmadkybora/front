<template>
    <!-- Footer -->
    <ftr color="primary-color-dark" class="text-center font-small darken-2">
        <div class="pt-4">
            <mdb-btn
                    outline="white"
                    tag="a"
                    href="https://mdbootstrap.com/docs/vue/getting-started/download/"
                    target="_blank"
            >Download MDB <mdb-icon icon="download" class="ml-2"
            /></mdb-btn>
            <mdb-btn
                    outline="white"
                    tag="a"
                    href="https://mdbootstrap.com/education/bootstrap/"
                    target="_blank"
            >Start free tutorial <mdb-icon icon="graduation-cap" class="ml-2"
            /></mdb-btn>
        </div>
        <hr class="my4" />
        <div class="pb-4">
            <a href="#"><mdb-icon fab icon="facebook-square" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="twitter" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="youtube" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="google-plus" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="dribbble" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="pinterest" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="github" class="mr-3"/></a>
            <a href="#"><mdb-icon fab icon="codepen" class="mr-3"/></a>
        </div>
        <p class="footer-copyright mb-0 py-3 text-center">
            &copy; {{ new Date().getFullYear() }} Copyright:
            <a href="https://mdbootstrap.com/docs/vue/"> MDBootstrap.com </a>
        </p>
    </ftr>
    <!-- /Footer -->
</template>

<script>
    import {
        mdbBtn,
        mdbIcon,
        mdbFooter,
    } from "mdbvue";

    export default {
        name: "Footer",
        components: {
            mdbBtn,
            mdbIcon,
            ftr: mdbFooter
        }
    }
</script>

<style scoped>

</style>