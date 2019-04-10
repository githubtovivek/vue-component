<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!server">Please select server from left panel</p>
        <div v-else>
            <p>{{server.name}}&nbsp; {{server.details}} <b>&nbsp; {{server.status}}</b></p>
            <hr>
            <button @click="changeServerStatus()">Change server Status</button>
        </div>
    </div>
</template>

<script>
import { serverBus } from "../../main";

export default {
  data: function() {
    return {
      server: null
    };
  },
  created: function() {
    serverBus.$on("serverIsSelected", serverData => {
      this.server = serverData;
    });
  },
  methods: {
    changeServerStatus() {
      this.server.status = "Normal";
    }
  }
};
</script>

