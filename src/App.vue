<template>
  <div id="app">
    <div class="h6 mb-2">
     CLICK ON ICON :-
      <span >
        <b-icon
          :variant="logger[0].toggleColor"
          style="cursor:pointer"
          :icon="logger[0].toggleStatus"
          @click="toggleIcon"
        ></b-icon>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      logger: [{ toggleColor: "success", toggleStatus: "toggle-on" }]
    };
  },
  methods: {
    toggleIcon() {
      if (this.logger[0].toggleStatus === "toggle-on") {
        this.logger[0].toggleStatus = "toggle-off";
        this.logger[0].toggleColor = "danger";
      }
      else{
        this.logger[0].toggleStatus = "toggle-on";
        this.logger[0].toggleColor = "success";
      }
    }
  }
};
</script>

