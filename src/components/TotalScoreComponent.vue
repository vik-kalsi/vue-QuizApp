<script>
  export default {
    props: ['score'],
    methods: {
      StartAgain() {
        window.location.reload();
      }
    }
  }
</script>



<template>
  <div class="space-y-4">
      <h1 class="text-4xl">Final Score</h1>
      <h1 class="text-4xl">You've scored {{ score }} correct answers out of 10 questions ({{ (score/10)*100 }}%)</h1>
      <button class="mt-8 border-2 p-4 transition hover:scale-105" v-on:click="StartAgain">Start Again</button>
  </div>
</template>