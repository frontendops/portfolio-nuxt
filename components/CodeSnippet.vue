<template>
    <div class="code-snippet">
        <ol class="code-snippet__list">
            <li class="code-snippet__code-line">
                <span class="code-snippet__line-number">1</span>
                <span class="code-snippet__code"><mark class="variable-name">const</mark>
                {{ challengeName}} = {</span>
            </li>
            <li class="code-snippet__code-line">
                <span class="code-snippet__line-number">2</span>
                <span class="code-snippet__code">difficulty: {{ difficulty }},</span>
            </li>
            <li class="code-snippet__code-line">
                <span class="code-snippet__line-number">3</span>
                <span class="code-snippet__code">concepts: [</span>
            </li>
            <li class="code-snippet__code-line"
                v-for="(concept, index) in concepts"
                :key="index">
                <span class="code-snippet__line-number">{{ 3 + index + 1 }}</span>
                <span class="code-snippet__code"><mark class="concept-name">'{{ concept }},'</mark></span>
            </li>
            <li class="code-snippet__code-line">
                <span class="code-snippet__line-number">{{concepts.length + 4}}</span>
                <span class="code-snippet__code">]</span>
            </li>
        </ol>
    </div>
</template>

<script>
export default {
    name: 'CodeSnippet',
    props: {
        difficulty: String,
        concepts: Array,
        challengeName: String
    }
}
</script>

<style lang="scss">

.code-snippet {
    color: white;
    background-color: #212A2E;
    border-radius: 1rem;

    &__list {
        padding-left: 0px;
        margin: 0;
    }

    &__list > li:first-child {
        .code-snippet__line-number {
            border-top-left-radius: 1rem;
        }
    }

    &__list > li:last-child {
        .code-snippet__line-number {
            border-bottom-left-radius: 1rem;
        }
    }

    &__line-number {
        background-color: #13161A;
        padding: 0.75rem;
        color: #707070;
    }

    &__code-line {
        display: flex;
    }

    &__code {
        background-color: #212A2E;
        display: flex;
        align-items: center;
        padding: 0.75rem;
    }
}

.variable-name {
    color: #66D9EF;
    background: none;
    padding-right: 0.4rem;
}

.concept-name {
    color: #FD971F;
    background: none;
    padding-left: 2rem;
}


</style>