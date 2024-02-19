<script>
export default {
  emits: ['HideQ9', 'updateScoreQ9'],
  data() {
    return {
      Question: "How many countries are in Scandinavia?",
    };
  },
  methods: {
    Q9Correct() {
        alert("Correct Answer");
        this.$emit("HideQ9");
        this.$emit("updateScoreQ9");
    },
    Q9Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ9");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 9: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q9Wrong"> 2 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q9Correct"> 3 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q9Wrong"> 4 </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q9Wrong"> 5 </button>
  </div>

</template>