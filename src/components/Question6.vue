<script>
export default {
  emits: ['HideQ6', 'updateScoreQ6'],
  data() {
    return {
      Question: "What is the capital of Australia?",
    };
  },
  methods: {
    Q6Correct() {
        alert("Correct Answer");
        this.$emit("HideQ6");
        this.$emit("updateScoreQ6");
    },
    Q6Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ6");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 6: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q6Correct"> Canberra </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q6Wrong"> Sydney </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q6Wrong"> Melbourne </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q6Wrong"> Brisbane </button>
  </div>

</template>