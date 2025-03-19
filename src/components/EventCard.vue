<template>
  <div class="event-card">
    <span>le {{ event.date }} à {{ event.time }}</span>
    <h4>{{ event.title }}</h4>
  </div>
</template>

<script>
export default {
  name: 'EventCard',
  data() {
    return {
      event: {
        id: 11001,
        category: 'Promotion',
        title: 'Portes ouvertes',
        description: 'Présentation des activités de la filière au public',
        location: 'nos locaux',
        date: '25 novembre 2024',
        time: '08:00',
      },
    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.event-card {
  padding: 20px;
  width: 250px;
  cursor: pointer;
  border: 1px solid #39495c;
  margin-bottom: 18px;
}
.event-card:hover {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
</style>
