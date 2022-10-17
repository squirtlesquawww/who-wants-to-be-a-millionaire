<template>
    <div class="text-3xl">
        {{ question }}

        <div class="grid grid-cols-2 gap-4">
            <div>A. {{ answerA }}</div>
            <div>B. {{ answerB }}</div>
            <div>C. {{ answerC }}</div>
            <div>D. {{ answerD }}</div>
        </div>

        <!-- <input type="text" v-model="question2"> -->
        <!-- {{ question2 }} -->
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
            question2: 'slafdjskdlf'
        }
    }
}
</script>
  