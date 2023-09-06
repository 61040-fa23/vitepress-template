---
layout: doc
---

<script setup>
  import {data as blogs} from './blogs/blog.data';
  import { withBase } from 'vitepress';
</script>

# Blogs

<ul v-if="blogs.length > 0">
  <li v-for="blog of blogs">
    <a :href="withBase(blog.url)">{{ blog.frontmatter.title }}</a>
  </li>
</ul>
<p v-else>
  Nothing here yet!
</p>
