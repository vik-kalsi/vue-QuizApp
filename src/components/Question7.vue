<script>
export default {
  emits: ['HideQ7', 'updateScoreQ7'],
  data() {
    return {
      Question: "What is the biggest state in India?",
    };
  },
  methods: {
    Q7Correct() {
        alert("Correct Answer");
        this.$emit("HideQ7");
        this.$emit("updateScoreQ7");
    },
    Q7Wrong() {
        alert("Wrong Answer");
        this.$emit("HideQ7");
    }
  }
};
</script>

<template>

    
  <div>
    <h1 class="text-4xl"> Question 7: {{ Question }} </h1>
  </div>

  <div class="grid space-y-6 mt-8 text-3xl">
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q7Wrong"> Karnataka </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q7Wrong"> Maharashtra </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q7Wrong"> Gujarat </button>
      <button class="border-2 p-2 transition hover:scale-105" v-on:click="Q7Correct"> Rajasthan </button>
  </div>

</template>