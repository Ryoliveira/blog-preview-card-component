<template>

    <h1 class="sr-only">Blog Preview Card Component</h1>

    <!-- container -->
    <main class="container">

        <h2 class="sr-only">Blog Preview Card Details</h2>

        <!-- blog svg -->
        <img class="illustration" :src="cardInfo?.illustration" alt="Blog card main illustration" />

        <!-- category tag -->
        <p class="category-tag" aria-label="category">{{ cardInfo?.tag }}</p>

        <!-- publish date -->
        <p class="publish-date" aria-label="publish date">{{ cardInfo?.publishDate }}</p>

        <!-- title -->
        <h2 class="title">{{ cardInfo?.title }}</h2>

        <!-- description -->
        <p class="description-text">{{ cardInfo?.description }}</p>

        <!-- author -->
        <div class="author-container" aria-label="Author information">
            <img class="avatar" :src="cardInfo?.avatar" alt="Author Avatar" />
            <span class="author-name">{{ cardInfo?.authorName }}</span>
        </div>

    </main>

    <footer role="contentinfo">
        <span>
            Frontend Mentor Challenge <a :href="solutionUrl" target="_blank">Blog Preview Card</a>.
            <span class="sr-only">(opens link to new tab)</span>
        </span>
        <br />
        <span>
            Coded By <a :href="githubUrl" target="_blank">Ryan Oliveira</a>.
            <span class="sr-only">(opens link to new tab)</span>
        </span>
    </footer>

</template>

<script setup lang="ts">
import { PropType } from 'vue';
import { BlogCardInfo } from '../interfaces/types.ts';

const solutionUrl = "https://www.frontendmentor.io/solutions/blog-preview-card-vue-component-written-in-typescript-gjnTDKPrCo";
const githubUrl = "https://github.com/Ryoliveira"

defineProps({
    // use PropType when using an interface
    cardInfo: {
        type: Object as PropType<BlogCardInfo>,
        required: true
    }
})
</script>


<style src="../scss/blog_preview_card.scss" scoped />