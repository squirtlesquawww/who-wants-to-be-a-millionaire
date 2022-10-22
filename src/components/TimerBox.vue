<template>
  <div
    class="
      text-3xl
      border-2 border-solid border-slate-500
      bg-black
      text-white text-right
    "
  >
    timer
    {{ seconds }} {{ remainingTime }}
  </div>
</template>
  
<script>
import moment from "moment";

export default {
  name: "TimerBox",
  props: {
    seconds: { type: Number, required: true },
  },
  data: () => {
    return {
      expiredTime: 0,
      remainingTime: 0,
      timeout: null,
    };
  },
  mounted() {
    this.expiredTime = moment().add(this.seconds, "s");
    this.remainingTime = moment
      .duration(this.expiredTime.diff(moment()))
      .asSeconds();

    this.startTimer();
  },
  methods: {
    startTimer() {
      if (this.remainingTime > 0) {
        this.timeOut = setTimeout(() => {
          this.remainingTime = moment
            .duration(this.expiredTime.diff(moment()))
            .asSeconds();
          this.startTimer();
        });
      } else {
        this.$emit("timeOut");
      }
    },
    decrementRemainingTime() {
      this.remainigTime = this.remainingTime - 1000;
      //   this.remainingTime -= 1000;
    },
  },
  beforeUnmount() {
    clearTimeout(this.timeOut);
  },
};
</script>
  