<template>
  <div :class="$style.card">
    <span
      :class="$style.name"
      v-text="event.name"
    ></span>

    <span
      :class="$style.description"
      v-text="event.description"
    ></span>

    <calendar
      :class="$style.calendar"
      :timestamp="this.event.datetime"
    ></calendar>
  </div>
</template>

<script>
  import Calendar from './calendar';

  export default {
    components: {
      Calendar
    },
    props: {
      /**
       * The event data object
       *
       * @type {Object}
       * @required
       */
      event: {
        type: Object,
        required: true
      }
    }
  };
</script>

<style lang="scss" module>
  .card {
    padding: 15px;
    background: #fff;
    margin: 10px 0;
    text-align: left;
    position: relative;
  }

  .name {
    font-size: 1.5em;
    font-weight: bold;
    display: block;
    margin-bottom: 10px;
  }

  .description {
    display: block;
  }

  .calendar {
    top: 10px;
    right: 10px;
    position: absolute;
  }
</style>
