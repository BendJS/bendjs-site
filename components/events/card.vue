<template>
  <div :class="$style.card">
    <a
      :class="$style.name"
      :href="event.link"
      target="_blank"
      v-text="event.name"
    ></a>

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
    padding: 25px;
    background: #fff;
    margin: 10px 0;
    text-align: left;
    position: relative;
    transition: box-shadow ease .4s;

    &:hover {
      box-shadow: 0 7px 14px 0 rgba(50,50,93,.1), 0 3px 6px 0 rgba(0,0,0,.07);
    }
  }

  .name {
    color: #323330;
    font-size: 1.5em;
    font-weight: bold;
    display: block;
    margin-bottom: 10px;
    text-decoration: none;

    &:hover {
      color: #f13a59;
    }
  }

  .description {
    display: block;
    margin-top: 15px;
  }

  .calendar {
    top: 15px;
    right: 15px;
    position: absolute;
  }
</style>
