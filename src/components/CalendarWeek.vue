<template>
  <div id="calendar-week" class="container">
    <div class="columns is-mobile">
      <CalendarDay v-for="day in sharedState.seedData" :key="day.id" :day="day">
      </CalendarDay>
    </div>
  </div>
</template>

<script>
import { store } from '../store.js';
import CalendarDay from './CalendarDay';

export default {
  name: 'CalendarWeek',
  components: {
    CalendarDay,
  },
  data() {
    return {
      sharedState: store.state,
    };
  },
};
</script>

<style lang="css" scoped>
#calendar-week {
  margin-bottom: 50px;
  margin-top: 15%;
}
.column {
  padding: 0 0 0 0;
}
</style>
