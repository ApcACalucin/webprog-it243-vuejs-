<template>
  <div class="comment">
    <p><strong>{{ author }}</strong></p>
    <p>{{ body }}</p>
  </div>
</template>

<script>
export default {
  name: 'Comment',
  props: {
    author: String,
    body: String
  }
}
</script>