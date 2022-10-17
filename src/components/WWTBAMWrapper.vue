<template>
  <div>
    <QuestionBlock question="who the top scorer in NBA?" answerA="kobe" answerB="jerrik" answerC="kareem"
      answerD="magic" />

    <div v-for="(question, index) in questions" :key="index">
      <QuestionBlock :question="question.question" :answerA="question.answerA" :answerB="question.answerB"
        :answerC="question.answerC" :answerD="question.answerD" />

    </div>
  </div>
</template>

<script>
import QuestionBlock from './QuestionBlock.vue';

export default {
  name: "WWTBAMWrapper",
  components: { QuestionBlock },
  data: () => {
    return {
      questions: [
        {
          question: 'Question 1',
          answerA: 'Answer A',
          answerB: 'Answer B',
          answerC: 'Answer C',
          answerD: 'Answer D'
        },
        {
          question: 'Question 2',
          answerA: 'Answer A',
          answerB: 'Answer B',
          answerC: 'Answer C',
          answerD: 'Answer D'
        },
        {
          question: 'Question 3',
          answerA: 'Answer A',
          answerB: 'Answer B',
          answerC: 'Answer C',
          answerD: 'Answer D'
        }
      ]
    }
  }
}
</script>
