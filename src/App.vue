<template>
  <BlogPreviewCard :card-info="cardInfo" />
</template>

<script setup lang="ts">
import BlogPreviewCard from './components/BlogPreviewCard.vue';
import { BlogCardInfo } from './interfaces/types';

import illustrationAricle from './assets/images/illustrationArticle.svg';
import avatar from './assets/images/image-avatar.webp';

const cardInfo: BlogCardInfo = {
  illustration: illustrationAricle,
  tag: 'Learning',
  publishDate: 'Published 21 Dec 2023',
  title: 'HTML & CSS foundations',
  description: 'These languages are the backbone of every website, defining structure, content, and presentation.',
  avatar: avatar,
  authorName: 'Greg Hooper',
}
</script>
