<template>
  <div>
    <h1>Create an Event, {{ user.name }}</h1>
    <p>created by, {{ user.id }}</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }},{{ catLength }}</li>
    </ul>
    <p>{{ getEventById(2) }}</p>
  </div>
</template>

<script>
import { mapGetters, mapState } from 'vuex'
export default {
  computed: {
    ...mapGetters(['getEventById']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style lang="scss" scoped></style>
