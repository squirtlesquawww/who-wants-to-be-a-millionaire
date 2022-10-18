<template>
    <div class="text-3xl border-2 border-solid border-slate-500 bg-black text-white text-right">
        $ {{ money }}
    </div>
</template>
  
<script>
export default {
    name: 'MoneyBox',
    props: {
        money: { type: Number, required: true },
    },
}
</script>
  