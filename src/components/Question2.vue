<script>
export default {
  emits: ['HideQ2', 'updateScoreQ2'],
  data() {
    return {
      Question: "How many states are there in USA?",
    };
  },
  methods: {
    Q2Correct() {
        alert("Correct Answer");
        this.$emit("HideQ2");
        this.$emit("updateScoreQ2");
    },
    Q2Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ2");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 2: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q2Wrong"> 48 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q2Wrong"> 52 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q2Correct"> 50 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q2Wrong"> 56 </button>
  </div>

</template>