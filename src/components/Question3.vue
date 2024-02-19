<script>
export default {
  emits: ['HideQ3', 'updateScoreQ3'],
  data() {
    return {
      Question: "What country do the Canary Islands belong to?",
    };
  },
  methods: {
    Q3Correct() {
        alert("Correct Answer");
        this.$emit("HideQ3");
        this.$emit("updateScoreQ3");
    },
    Q3Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ3");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 3: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q3Wrong"> Portugal </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q3Wrong"> France </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q3Wrong"> Greece </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q3Correct"> Spain </button>
  </div>

</template>