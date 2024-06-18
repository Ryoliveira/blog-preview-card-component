<template>

    <h1 class="sr-only">Blog Preview Card Component</h1>

    <!-- container -->
    <div class="container">

        <h2 class="sr-only">Blog Preview Card Details</h2>
        <main>
            <!-- blog svg -->
            <img class="illustration" :src="cardInfo?.illustration"
                alt="Various shapes and lines with a html closing tag and open curly braces" />

            <!-- category tag -->
            <a href="#" class="category-tag">
                {{ cardInfo?.category }}
                <span class="sr-only">(Navigates to new page)</span>
            </a>

            <!-- publish date -->
            <p class="publish-date">{{ cardInfo?.publishDate }}</p>

            <!-- title -->
            <a class="title" href="#">
                {{ cardInfo?.title }}
                <span class="sr-only">(Navigates to new page)</span>
            </a>

            <!-- description -->
            <p class="description-text">{{ cardInfo?.description }}</p>

            <!-- author -->
            <div class="author-container">
                <img class="avatar" :src="cardInfo?.avatar"
                    alt="Head shot of caucasian man smiling with brown hair while wearing a light blue shirt and looking off to the side" />
                <span class="author-name">{{ cardInfo?.authorName }}</span>
            </div>
        </main>
    </div>

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