<script>
export default {
  emits: ['HideQ4', 'updateScoreQ4'],
  data() {
    return {
      Question: "How many countries are there in Oceania?",
    };
  },
  methods: {
    Q4Correct() {
        alert("Correct Answer");
        this.$emit("HideQ4");
        this.$emit("updateScoreQ4");
    },
    Q4Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ4");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 4: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q4Wrong"> 13 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q4Correct"> 14 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q4Wrong"> 15 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q4Wrong"> 16 </button>
  </div>

</template>