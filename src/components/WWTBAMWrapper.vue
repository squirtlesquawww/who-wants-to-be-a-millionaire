<template>
  <div class="bg-black min-h-screen">
    <MoneyBox money="1" />
    <QuestionBlock question="who the top scorer in NBA?" answerA="kobe" answerB="jerrik" answerC="kareem"
      answerD="magic" />
    <MoneyList />
  </div>
</template>

<script>
import QuestionBlock from './QuestionBlock.vue';
import MoneyBox from './MoneyBox.vue';
import MoneyList from './MoneyList.vue';

export default {
  name: "WWTBAMWrapper",
  components: { QuestionBlock, MoneyBox, MoneyList },
  data: () => {
    return {
      questions: [

      ]
    }
  }
}
</script>
