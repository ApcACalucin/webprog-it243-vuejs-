<template>
  <div class="comment-form">
    <input v-model="author" placeholder="Your name" />
    <textarea v-model="body" placeholder="Write a comment..."></textarea>
    <button @click="submit">Submit</button>
  </div>
</template>

<script>
export default {
  name: 'CommentForm',
  data() {
    return {
      author: '',
      body: ''
    }
  },
  methods: {
    submit() {
      if (!this.author || !this.body) return
      this.$emit('add-comment', { author: this.author, body: this.body })
      this.author = ''
      this.body = ''
    }
  }
}
</script>