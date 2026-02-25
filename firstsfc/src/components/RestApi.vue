<template>
  <div class="rest-api">
    <button @click="fetchData">Fetch Comments</button>
    <div v-if="loading">Loading...</div>
    <div v-if="error" class="error">{{ error }}</div>
    <ul v-if="items.length">
      <li v-for="item in items" :key="item.id">
        <comment :author="item.email" :body="item.body" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'RestApi',
  data() {
    return {
      items: [],
      loading: false,
      error: null
    }
  },
  methods: {
    async fetchData() {
      this.loading = true
      this.error = null
      try {
        const res = await fetch('https://jsonplaceholder.typicode.com/comments?_limit=10')
        if (!res.ok) throw new Error('Failed to fetch')
        this.items = await res.json()
      } catch (err) {
        this.error = err.message
      } finally {
        this.loading = false
      }
    }
  }
}
</script>