<template>
  <container>
    <div>
      <img width="500" src="images/bendjs-logo.png" alt="">
    </div>

    <events-list></events-list>
  </container>
</template>

<script>
import Container from '~/components/layout/container.vue';
import EventsList from '~/components/events/list.vue';

export default {
  components: {
    Container,
    EventsList
  }
};
</script>

