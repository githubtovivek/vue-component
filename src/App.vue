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
            servers: [
                {id: 1, name:"Google", status: "Normal", details: "google server"},
                {id: 2, name:"Yahoo", status: "critical", details: "Yahoo server"},
                {id: 3, name:"Amazon", status: "critical", details: "Amazon server"},
                {id: 4, name:"Facebook", status: "Normal", details: "Facebook server"},
                {id: 5, name:"Orkut", status: "unknown", details: "Orkut server"},
                {id: 6, name:"Fedid", status: "critical", details: "Fedid server"}
            ]
        };
    }
}
</script>

<style>

</style>
