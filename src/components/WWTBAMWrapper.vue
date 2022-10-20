<template>
  <div class="bg-black min-h-screen">
    <div class="grid grid-cols-3">
      <div class="col-span-2">
    
    <QuestionBlock question="who the top scorer in NBA?" answerA="kobe" answerB="jerrik" answerC="kareem"
      answerD="magic" />
     <div class="grid grid-cols-2">
      <div>
        <TimerBox />
      </div>
      <div>
        <LifeLineButtons/>
        <MoneyBox money="1" />
      </div>
     </div>
      </div>
    <MoneyList />
  </div>
  </div>
</template>

<script>
import QuestionBlock from './QuestionBlock.vue';
import MoneyBox from './MoneyBox.vue';
import MoneyList from './MoneyList.vue';
import TimerBox from './TimerBox.vue';
import LifeLineButtons from './LifeLineButtons.vue';

export default {
  name: "WWTBAMWrapper",
  components: { QuestionBlock, MoneyBox, MoneyList, TimerBox, LifeLineButtons },
  data: () => {
    return {
      questions: [

      ]
    }
  }
}
</script>
