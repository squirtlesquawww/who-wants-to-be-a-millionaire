<template>
  <div class="bg-black min-h-screen">
    <div class="grid grid-cols-3">
      <div class="col-span-2">
        <QuestionBlock
          question="who the top scorer in NBA?"
          answerA="kobe"
          answerB="jerrik"
          answerC="kareem"
          answerD="magic"
        />
        <div class="grid grid-cols-2">
          <div>
            <TimerBox
              :seconds="questionsToSecondsMap[currentQuestion.number]"
            />
          </div>
          <div>
            <LifeLineButtons />
            <MoneyBox money="1" />
          </div>
        </div>
      </div>
      <MoneyList :amounts="amounts" />
    </div>
  </div>
</template>

<script>
import QuestionBlock from "./QuestionBlock.vue";
import MoneyBox from "./MoneyBox.vue";
import MoneyList from "./MoneyList.vue";
import TimerBox from "./TimerBox.vue";
import LifeLineButtons from "./LifeLineButtons.vue";

export default {
  name: "WWTBAMWrapper",
  components: { QuestionBlock, MoneyBox, MoneyList, TimerBox, LifeLineButtons },
  data: () => {
    return {
      amounts: [
        100, 200, 300, 500, 1000, 2000, 4000, 8000, 16000, 32000, 64000, 125000,
        250000, 500000, 1000000,
      ],
      currentQuestion: {
        number: 1,
        question: "who the top scorer in NBA?",
        answers: [
          {
            answer: "kobe",
            correct: false,
          },
          {
            answer: "jerrik",
            correct: false,
          },
          {
            answer: "kareem",
            correct: true,
          },
          {
            answer: "noah",
            correct: false,
          },
        ],
      },
      questions: [],
      questionsToSecondsMap: {
        1: 15,
        2: 15,
        3: 15,
        4: 15,
        5: 15,
        6: 30,
        7: 30,
        8: 30,
        9: 30,
        10: 30,
        11: 45,
        12: 45,
        13: 45,
        14: 45,
        15: 45,
      },
      remainingSeconds: 0,
    };
  },
};
</script>
