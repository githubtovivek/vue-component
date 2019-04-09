<template>
    <div class="container">
        <app-header></app-header>
        <hr>
        <div class="row">
            <app-server-status></app-server-status>
            <app-server-Details></app-server-Details>
        </div>
        <hr>
        <app-footer></app-footer>
    </div>
</template>

<script>
import Header from './components/shared/Header.vue'
import ServerStatus from './components/server/ServerStatus.vue'
import Footer from './components/shared/Footer.vue'
import serverDetails from './components/server/ServerDetails.vue'

export default {
    components: {
        'app-header': Header,
        'app-server-status': ServerStatus,
        'app-footer': Footer,
        'app-server-Details': serverDetails
    }
}
</script>

<style>

</style>
