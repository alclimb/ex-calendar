<template>
  <div class="app-calendar" style="width: 300px">
    <div class="day-container">
      <span class="day day-prev-month">30</span>
      <span class="day">1</span>
      <span class="day">2</span>
      <span class="day">3</span>
      <span class="day">4</span>
      <span class="day">5</span>
      <span class="day">6</span>
      <span class="day">7</span>
      <span class="day">8</span>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "@nuxtjs/composition-api";

export default defineComponent({});
</script>

<style lang="scss" scoped>
.app-calendar {
  .day-container {
    display: flex;
    text-align: center;
    flex-wrap: wrap;

    border: 1px solid #ccc;

    .day {
      width: unquote("calc(100% * 1 / 7.001)");
      //border: 1px solid transparent;
      border-radius: 150px;

      &:hover {
        cursor: pointer;
        outline: 0;
        background: #e6e6e6;
        border-color: #e6e6e6;
      }
    }

    .day-prev-month {
      color: rgba(57, 57, 57, 0.3);
      background: transparent;
      border-color: transparent;
      cursor: default;
    }
  }
}
</style>
