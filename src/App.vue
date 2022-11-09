<template>
  <div class="wrapper">
    <header class="header">
      <h1 class="title">Bienvenido a Tweepter</h1>
    </header>
    <List />
  </div>
</template>

<script>
import List from './components/List.vue'

export default {
  name: 'App',
  components: {
    List,
  }
}
</script>
