<template>
  <ul>
    <knowledge-element
      v-for="topic in topics"
      :key="topic.id"
      :id="topic.id"
      :topic-name="topic.title"
      :description="topic.description"
    ></knowledge-element>
  </ul>
</template>

<script>
export default {
  inject: ['topics'],
  data () {
    return {
      topicSelected: null,
    };
  },
  provide() {
    return {
      selectedTopic: this.topicSelected,
    }
  },
  methods: {
    onSelectTopic(id) {
      this.topicSelected = this.topics.find(topic => topic.id === id);
    },
  },
};
</script>