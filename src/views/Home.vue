<template>
  <div class="home">
    <Figma :figma="figmaConfig" v-model="viewModel" :config="config"/>
  </div>
</template>


<script>
import Vue from "vue";
import Figma from "vue-low-code";
Vue.use(Figma);

// import JSON file for deployment
// import app from './app.json'

export default {
  name: "Home",
  data: function () {
    return {
      // figmaJSON: app,
      figmaConfig: {
        figmaFile: "uKgt9PzMeazuh8SqXJQoVs",
        figmaAccessKey: "188835-f78a3047-5333-45c7-bdf0-4d426ebf3277",
      },
      viewModel: {
        /**
         * Add your view model here
         */
      },
      config: {
        responsive: [
          { value: "Desktop", label: "Desktop", types: ["desktop"] },
          { value: "Mobile", label: "Mobile", types: ["tablet", "mobile"] },
        ],
        components: {
          /**
           * Register custom components here
           */
        },
      },
    };
  },
  components: {},
  methods: {
    /**
     * Place your methods here
     */
  },
  mounted () {
    console.log(this.$router.mode, "router mode")
    console.log(this.$router, "router")

    console.debug(this.$router.mode, "router mode")
    console.debug(this.$router, "router")
  }
};
</script>
