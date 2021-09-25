<template>
  <section>
    <h2>{{ title }}</h2>
    <p>{{ fullText }}</p>
  </section>
</template>

<script>
export default {
  props: ['title', 'fullText'],
  // inject: ['selectedTopic']
};
</script>