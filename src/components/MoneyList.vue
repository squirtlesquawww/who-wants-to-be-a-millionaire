<template>
  <div
    class="
      text-3xl
      border-2 border-solid border-slate-500
      bg-black
      text-white text-right
    "
  >
    <div
      class="
        text-3xl
        border-2 border-solid border-slate-500
        bg-black
        text-white text-right
        flex
        justify-between
        px-10
      "
      :class="{ 'bg-yellow-600': activeAmount === index }"
      v-for="(amount, index) in reversedAmounts()"
      :key="amount"
    >
      {{ amounts.length - index }}
      <div>${{ amount }}</div>
    </div>
  </div>
</template>
             
<script>
export default {
  name: "MoneyList",
  props: {
    activeAmount: { type: Number, required: false, default: 0 },
  },
  data: () => {
    return {
      amounts: [
        100, 200, 300, 500, 1000, 2000, 4000, 8000, 16000, 32000, 64000, 125000,
        250000, 500000, 1000000,
      ],
      // items: [{ message: 'Foo' }, { message: 'Bar' }]
    };
  },
  methods: {
    reversedAmounts() {
      let reversedArray = [...this.amounts].reverse();
      return reversedArray;
      // return this.amounts.reverse();
    },
  },
};
</script>
             