<template>
  <div :class="$style.calendar">
    <span :class="$style.day" v-text="calendarDay"></span>
    <span :class="$style.month" v-text="calendarMonth"></span>
  </div>
</template>

<script>
  import moment from 'moment';

  export default {
    props: {
      /**
       * The timestamp
       *
       * @type {String}
       * @required
       */
      timestamp: {
        type: String,
        required: true
      }
    },

    computed: {
      /**
       * Returns the day from moment.
       *
       * @return {String}
       */
      calendarDay () {
        return moment(this.timestamp).format('D');
      },

      /**
       * Returns the month from moment.
       *
       * @return {String}
       */
      calendarMonth () {
        return moment(this.timestamp).format('MMM');
      }
    }
  };
</script>

<style lang="scss" module>
  .calendar {
    background: #f6f7f8;
    border: 1px solid rgba(46, 62, 72, .12);
    border-radius: 8px;
    color: #fff;
    padding: 8px;
    font-size: .75em;
    width: 50px;
    height: 50px;
    display: flex;
    flex-wrap: wrap;
    text-align: center;
    align-content: center;
    justify-content: center;

    .day {
      color: #f13a59;
      font-weight: bold;
      font-size: 1.75em;
      margin-bottom: -3.5px;
    }

    .month {
      color: rgba(46, 62, 72, .6);
      font-size: 1em;
      text-transform: uppercase;
      font-weight: 500;
    }
  }
</style>
