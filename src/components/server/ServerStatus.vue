<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li class="list-group-item" v-for="(server, index) in appServers" :key = "index">
                ({{ index }})&nbsp;{{ server }} 
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props: ["appServers"]
}
</script>

<style>
 div {
     border: 2px solid grey;
 }
</style>


