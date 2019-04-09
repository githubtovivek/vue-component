<template>
    <div class="container" v-if="servers.length > 0">
        <app-header></app-header>
        <hr>
        <div class="row">
            <app-server-status :appServers = "servers"></app-server-status>
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
    },
    data: function() {
        return {
            servers: ["Google", "Yahoo", "Amazon", "Facebook", "Orkut", "Fedid"]
        };
    }
}
</script>

<style>

</style>
