<script setup>
import { ref, onMounted } from 'vue'
import { supabase } from './lib/supabaseClient' // Path to your connection file
import PersonalProfile from './components/PersonalProfile.vue' // Path to the code you just sent

const instruments = ref([])

async function getInstruments() {
  const { data } = await supabase.from('instruments').select()
  instruments.value = data
}

onMounted(() => {
  getInstruments()
})
</script>

<template>
  <div id="app-wrapper">
    <PersonalProfile />

    <hr class="divider" />

    <section class="database-content">
      <h2>Instruments List</h2>
      <ul>
        <li v-for="instrument in instruments" :key="instrument.id">
          {{ instrument.name }}
        </li>
      </ul>
    </section>
  </div>
</template>

<style>
.divider { margin: 40px 0; border: 1px solid #eee; }
.database-content { text-align: center; }
</style>