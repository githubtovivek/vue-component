<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
           <appServer v-for= "server in getServers()" :key = "server.id" :server = server></appServer>
        </ul>
    </div>
</template>

<script>
import server from "./server.vue"

export default {
    props: {
        appServers: {
            type: Array,
            default: [
                {id: 1, name:"Google", status: "Normal", details: "google server"},
                {id: 2, name:"Yahoo", status: "critical", details: "Yahoo server"}
            ]
        }
    },
    methods: {
        getServers() {
            return this.appServers;
        }
    },
    components: {
        appServer: server
    }
}
</script>


