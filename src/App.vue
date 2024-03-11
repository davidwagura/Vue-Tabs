<template>
  <div>
    <button v-for="tab in tabs" :key="tab" @click="selected = tab;">
      {{ tab }}
    </button>

    <component :is="selected"></component>
  </div>
</template>

<script>
import Home from "./components/Home.vue";
import Contact from "./components/Contact.vue";

export default {
  data: function() {
    return {
      tabs: ["Home", "Contact"],
      selected: "Home"
    };
  },
  components: {
    Home,
    Contact
  }
};
</script>