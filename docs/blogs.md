---
layout: doc
---

<script setup>
  import {data as blogs} from './blogs/blog.data';
</script>

# Blogs

<ul v-if="blogs.length > 0">
  <li v-for="blog of blogs">
    <a :href="blog.url">{{ blog.frontmatter.title }}</a>
  </li>
</ul>
<p v-else>
  Nothing here yet!
</p>