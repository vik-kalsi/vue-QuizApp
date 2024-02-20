<script>
import Question1 from './components/Question1.vue'
import Question2 from './components/Question2.vue'
import Question3 from './components/Question3.vue'
import Question4 from './components/Question4.vue'
import Question5 from './components/Question5.vue'
import Question6 from './components/Question6.vue'
import Question7 from './components/Question7.vue'
import Question8 from './components/Question8.vue'
import Question9 from './components/Question9.vue'
import Question10 from './components/Question10.vue'
import TotalScoreComponent from './components/TotalScoreComponent.vue'

export default{
  components: {
    Question1,
    Question2,
    Question3,
    Question4,
    Question5,
    Question6,
    Question7,
    Question8,
    Question9,
    Question10,
    TotalScoreComponent,
  },
data() {  
    return {
      showScore: true,
      showQuestion1: true,
      showQuestion2: false,
      showQuestion3: false,
      showQuestion4: false,
      showQuestion5: false,
      showQuestion6: false,
      showQuestion7: false,
      showQuestion8: false,
      showQuestion9: false,
      showQuestion10: false,
      ShowTotalScoreComponent: false,
      score: 0
    };
  },
  methods: {
    HideQuestion1() {
      this.showQuestion1 = false
      this.showQuestion2 = true
    },
    HideQuestion2() {
      this.showQuestion2 = false
      this.showQuestion3 = true
    },
    HideQuestion3() {
      this.showQuestion3 = false
      this.showQuestion4 = true
    },
    HideQuestion4() {
      this.showQuestion4 = false
      this.showQuestion5 = true
    },
    HideQuestion5() {
      this.showQuestion5 = false
      this.showQuestion6 = true
    },
    HideQuestion6() {
      this.showQuestion6 = false
      this.showQuestion7 = true
    },
    HideQuestion7() {
      this.showQuestion7 = false
      this.showQuestion8 = true
    },
    HideQuestion8() {
      this.showQuestion8 = false
      this.showQuestion9 = true
    },
    HideQuestion9() {
      this.showQuestion9 = false
      this.showQuestion10 = true
    },
    HideQuestion10() {
      this.showQuestion10 = false
      this.showScore = false
      this.ShowTotalScoreComponent = true
    },
    updateScore(){
      this.score++
    }
  }
}
</script>


<template>
  <div v-show="showScore" class="flex justify-center text-6xl">
    <h1>Score is {{ score }}</h1>
  </div>

  <div v-show="showQuestion1" class="border-2 p-8 my-12">
    <Question1 @HideQ1="HideQuestion1" @updateScoreQ1="updateScore"/>
  </div>

  <div v-show="showQuestion2" class="border-2 p-8 my-12">
    <Question2 @HideQ2="HideQuestion2" @updateScoreQ2="updateScore"/>
  </div>

  <div v-show="showQuestion3" class="border-2 p-8 my-12">
    <Question3 @HideQ3="HideQuestion3" @updateScoreQ3="updateScore"/>
  </div>

  <div v-show="showQuestion4" class="border-2 p-8 my-12">
    <Question4 @HideQ4="HideQuestion4" @updateScoreQ4="updateScore"/>
  </div>

  <div v-show="showQuestion5" class="border-2 p-8 my-12">
    <Question5 @HideQ5="HideQuestion5" @updateScoreQ5="updateScore"/>
  </div>

  <div v-show="showQuestion6" class="border-2 p-8 my-12">
    <Question6 @HideQ6="HideQuestion6" @updateScoreQ6="updateScore"/>
  </div>

  <div v-show="showQuestion7" class="border-2 p-8 my-12">
    <Question7 @HideQ7="HideQuestion7" @updateScoreQ7="updateScore"/>
  </div>

  <div v-show="showQuestion8" class="border-2 p-8 my-12">
    <Question8 @HideQ8="HideQuestion8" @updateScoreQ8="updateScore"/>
  </div>

  <div v-show="showQuestion9" class="border-2 p-8 my-12">
    <Question9 @HideQ9="HideQuestion9" @updateScoreQ9="updateScore"/>
  </div>

  <div v-show="showQuestion10" class="border-2 p-8 my-12">
    <Question10 @HideQ10="HideQuestion10" @updateScoreQ10="updateScore"/>
  </div>

  <div v-show="ShowTotalScoreComponent" class="border-2 p-8 my-12">
    <TotalScoreComponent :score="score"/>
  </div>
  
</template>