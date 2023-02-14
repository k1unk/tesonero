<template>
    <section class="answers-block">
        <div class="answers-wrapper">
            <div class="answers-above-header__line"/>
            <h1 class="answers__header">Lorem ipsum, dolor sit adipisicing elit.</h1>
            <p class="answers__subheader-text">Porro ab rerum omnis magnam eligendi error nobis dolore?</p>
            <ul class="answers-list">
                <Answer v-for="question in questions"
                        :key=question.id
                        :question=question
                        @toggleAnswer="toggleAnswer"
                />
            </ul>
        </div>
    </section>
</template>

<script>
import Answer from "@/components/AnswersSection/Answer";

export default {
    name: 'AnswersSection',
    components: {Answer},
    data() {
        return {
            openedIdNow: 0,
            questions: [
                {
                    id: 1,
                    imgSrc: "answers-1.svg",
                    question: "Lorem ipsum, dolor sit amet adipisicing elit.",
                    answer: "Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit " +
                        "exercitationem laborum cupiditate magnam eaque quae delenit",
                    isAnswerOpened: false
                },
                {
                    id: 2,
                    imgSrc: "answers-2.svg",
                    question: "Lorem ipsum, dolor sit amet adipisicing elit.",
                    answer: "Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit " +
                        "exercitationem laborum cupiditate magnam eaque quae delenit",
                    isAnswerOpened: false
                },
                {
                    id: 3,
                    imgSrc: "answers-3.svg",
                    question: "Lorem ipsum, dolor sit amet adipisicing elit.",
                    answer: "Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit " +
                        "exercitationem laborum cupiditate magnam eaque quae delenit",
                    isAnswerOpened: false
                },
                {
                    id: 4,
                    imgSrc: "answers-4.svg",
                    question: "Lorem ipsum, dolor sit amet adipisicing elit.",
                    answer: "Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit " +
                        "exercitationem laborum cupiditate magnam eaque quae delenit",
                    isAnswerOpened: false
                },
                {
                    id: 5,
                    imgSrc: "answers-5.svg",
                    question: "Lorem ipsum, dolor sit amet adipisicing elit.",
                    answer: "Laboriosam quas, aut consectetur animi autem aliquid consequuntur suscipit " +
                        "exercitationem laborum cupiditate magnam eaque quae delenit",
                    isAnswerOpened: false
                },
            ]
        }
    },
    methods: {
        toggleAnswer(question){
            if (this.openedIdNow===question.id) {
                this.openedIdNow = 0
                question.isAnswerOpened = false
                return
            }
            for (let i = 0; i < this.questions.length; i++) {
                if (this.questions[i].id===this.openedIdNow) {
                    this.questions[i].isAnswerOpened = false
                }
            }
            question.isAnswerOpened = true
            this.openedIdNow = question.id
        }
    },
}
</script>
