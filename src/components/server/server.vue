<template>
    <li class="list-group-item" :key = "index" @click="serverSelected()">
        ({{ server.id }})&nbsp;{{ server.name }} <b>(&nbsp;{{ server.status }}&nbsp;)</b>
    </li>
</template>

<script>
import { serverBus } from "../../main";

export default {
    props: ["server"],
    methods: {
        serverSelected() {
            serverBus.$emit("serverIsSelected", this.server)
        }
    }
}
</script>

<style>
    li.list-group-item {
        cursor: pointer;
    }
</style>


