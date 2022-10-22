<template>
    <div class="text-3xl border-2 border-solid border-slate-500 bg-blue-900 text-white">
        <div class="p-5">
            {{ question }}

        </div>
        <div class="grid grid-cols-2">
            <div class="border-2 border-solid border-slate-500 p-3" :class="{ 'bg-yellow-600': hoverA }"
                @mouseover="hoverA = true" @mouseleave="hoverA = false">
                <span class="text-amber-400">A.</span> {{ answerA }}
            </div>
            <div class="border-2 border-solid border-slate-500 p-3" :class="{ 'bg-yellow-600': hoverB }"
                @mouseover="hoverB = true" @mouseleave="hoverB = false">
                <span class="text-amber-400">B.</span> {{ answerB }}
            </div>
            <div class="border-2 border-solid border-slate-500 p-3" :class="{ 'bg-yellow-600': hoverC }"
                @mouseover="hoverC = true" @mouseleave="hoverC = false">
                <span class="text-amber-400">C.</span> {{ answerC }}
            </div>
            <div class="border-2 border-solid border-slate-500 p-3" :class="{ 'bg-yellow-600': hoverD }"
                @mouseover="hoverD = true" @mouseleave="hoverD = false">
                <span class="text-amber-400">D.</span> {{ answerD }}
            </div>
            {{ hover}}
        </div>
    </div>
</template>
  
<script>

export default {
    name: 'QuestionBlock',
    props: {
        question: { type: String, required: true },
        answerA: { type: String, required: true },
        answerB: { type: String, required: true },
        answerC: { type: String, required: true },
        answerD: { type: String, required: true },
    },
    data: () => {
        return {
            hoverA: false,
            hoverB: false,
            hoverC: false,
            hoverD: false
        }
    }
}
</script>
  
<!-- bg-yellow-600 -->