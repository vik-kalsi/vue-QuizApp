<script>
export default {
  emits: ['HideQ1', 'updateScoreQ1'],
  data() {
    return {
      Question: "What continent is Brazil located in?",
    };
  },
  methods: {
    Q1Correct() {
        alert("Correct Answer"),
        this.$emit("HideQ1");
        this.$emit("updateScoreQ1")
    },
    Q1Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ1");
    }
  }
};
</script>

<template>

    <div>
      <h1 class="text-4xl"> Question 1: {{ Question }} </h1>
    </div>

    <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q1Correct"> South America </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q1Wrong"> Europe </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q1Wrong"> Africa </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q1Wrong"> Asia </button>
    </div>

</template>