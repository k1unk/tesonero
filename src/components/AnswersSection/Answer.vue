<template>
    <li class="answers-item">
        <div class="answers-item-question">
            <div class="answers-item-question__left">
                <div class="answers-item-question__img">
                    <img :src="require(`@/assets/${question.imgSrc}`)" alt=""/>
                </div>
                <p :class='getQuestionTextClass()'>{{ question.question }}</p>
            </div>
            <div class="answers-item__arrow" @click="toggleAnswer(question)">
                <img src="@/assets/arrow-up.svg" alt="" v-if="question.isAnswerOpened">
                <img src="@/assets/arrow-down.svg" alt="" v-else>
            </div>
        </div>
        <div class="answers-item__answer" v-if="question.isAnswerOpened">
            <p>{{ question.answer }}</p>
        </div>
    </li>

</template>

<script>

export default {
    name: 'Answer',
    props: {
        question: Object
    },
    components: {},
    methods: {
        toggleAnswer(question) {
            this.$emit("toggleAnswer", question)
        },
        getQuestionTextClass(){
            return this.question.isAnswerOpened
                ? 'answers-item-question__text answers-item-question__text_opened'
                : 'answers-item-question__text'
        }
    },
}
</script>
