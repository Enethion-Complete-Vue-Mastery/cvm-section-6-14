<template>
  <app-form>
    <template v-slot:help>
      <p>{{ help }}</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="name" />
      <input type="text" placeholder="message" />
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
    Dummy
  </app-form>
  <app-form>
    <template v-slot:help>
      <p>Some help text</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="email" />
      <input type="text" placeholder="username" />
      <input type="password" placeholder="password" />
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
  </app-form>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import AppForm from './components/Form.vue'

export default defineComponent({
  name: 'App',
  components: {
    AppForm
  },
  data () {
    return {
      help: 'Dumby text' as string
    }
  }
})
</script>
