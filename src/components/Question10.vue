<script>
export default {
  emits: ['HideQ10', 'updateScoreQ10'],
  data() {
    return {
      Question: "What is the capital of Croatia?",
    };
  },
  methods: {
    Q10Correct() {
        alert("Correct Answer");
        this.$emit("HideQ10");
        this.$emit("updateScoreQ10");
    },
    Q10Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ10");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 10: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q10Wrong"> Dubrovnik </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q10Wrong"> Split </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q10Correct"> Zagreb </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q10Wrong"> Zadar </button>
  </div>

</template>