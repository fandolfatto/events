<template>
  <div class="events">
    <EventCard v-for="item in events" :event="item" :key="item.id"> </EventCard>
  </div>
</template>

<script>
// @ is an alias to /src
import EventCard from '@/components/EventCard.vue'
import axios from 'axios'

export default {
  name: 'HomeView',
  components: {
    EventCard,
  },
  data() {
    return {
      events: null,
    }
  },
  created() {
    axios
      .get(
        'http://my-json-server.typicode.com/fandolfatto/VueAPIOptions/events'
      )
      .then((response) => {
        this.events = response.data
      })
      .catch((error) => {
        console.log(error)
      })
  },
}
</script>

<style scoped>
.events {
  display: flex;
  flex-direction: column;
  align-items: center;
}
</style>
