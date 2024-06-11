<template>

    <!-- container -->
    <div class="container">

        <!-- blog svg -->
        <img class="illustration" :src="cardInfo?.illustration" alt="Blog Illustration" />

        <!-- topic tag -->
        <div class="topic-container">
            <span class="topic-tag">{{ cardInfo?.tag }}</span>
        </div>

        <!-- publish date -->
        <div class="publish-container">
            <span class="publish-date">{{ cardInfo?.publishDate }}</span>
        </div>


        <!-- title -->
        <div class="title-container">
            <h2 class="title">{{ cardInfo?.title }}</h2>
        </div>

        <!-- description -->
        <p class="description-text">{{ cardInfo?.description }}</p>

        <!-- author -->
        <div class="author-container">
            <img class="avatar" :src="cardInfo?.avatar" alt="Author Avatar"/>
            <span class="author-name">{{ cardInfo?.authorName }}</span>
        </div>
    </div>

</template>

<script setup lang="ts">
import { PropType } from 'vue';
import  { BlogCardInfo }  from '../interfaces/types.ts';


defineProps({
    // user PropType when using an interface
    cardInfo: {
        type: Object as PropType<BlogCardInfo>,
        required: true
    }
})
</script>


<style src="../scss/blog_preview_card.scss" scoped />