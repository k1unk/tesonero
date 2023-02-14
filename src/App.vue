<template>
    <div>
        <Header/>
        <PresentationSection/>
        <div class="quotes-and-answers">
            <QuotesSection/>
            <AnswersSection/>
        </div>
    </div>
</template>

<style lang="scss" src="./app.scss"></style>
<script>
import Header from "@/components/Header/Header";
import PresentationSection from "@/components/PresentationSection/PresentationSection";
import QuotesSection from "@/components/QuotesSection/QuotesSection";
import AnswersSection from "@/components/AnswersSection/AnswersSection";

export default {
    name: 'App',
    components: {
        Header, PresentationSection, QuotesSection, AnswersSection
    }
}
</script>
