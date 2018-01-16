<template>
  <div :class="$style['events-list']">
    <h1 :class="$style.title">Events</h1>
    <card
      v-for="event in events"
      :event="event"
      :key="event.id"
    ></card>
  </div>
</template>

<script>
  import events from '~/data/meetups';
  import Card from './card';

  export default {
    components: {
      Card
    },

    data () {
      return {
        events
      };
    }
  };
</script>

<style lang="scss" module>
  .events-list {
    margin-top: 60px;
    max-width: 650px;
    min-width: 650px;
  }

  .title {
    text-align: left;
    font-size: 3em;
  }
</style>
