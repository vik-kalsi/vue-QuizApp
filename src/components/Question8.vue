<script>
export default {
  emits: ['HideQ8', 'updateScoreQ8'],
  data() {
    return {
      Question: "What is the capital of Bavaria?",
    };
  },
  methods: {
    Q8Correct() {
        alert("Correct Answer");
        this.$emit("HideQ8");
        this.$emit("updateScoreQ8");
    },
    Q8Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ8");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 8: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q8Correct"> Munich </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q8Wrong"> Nuremberg </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q8Wrong"> Augsburg </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q8Wrong"> Fürth </button>
  </div>

</template>