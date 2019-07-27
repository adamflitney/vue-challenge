<template>
  <div class="employee-list">
    <img src="@/assets/the-godfather.svg" alt="godfather logo" />
    <ul>
      <li
        v-for="employee in employees"
        :key="employee.name"
        :class="{
          selected: isSelected(employee.name),
          colleague: isColleague(employee.name)
        }"
        @click="selectEmployee(employee.name)"
        :style="{ fontSize: 1 + employee.popularity / 2 + 'rem' }"
      >
        {{ employee.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: {
    employees: {
      type: Array,
      required: true
    },
    selected: {
      type: Object,
      required: true
    }
  },
  methods: {
    isSelected(employeeName) {
      if (employeeName === this.selected.name) {
        return true;
      } else {
        return false;
      }
    },
    isColleague(employeeName) {
      return this.selected.colleagues.find(colleague => {
        return colleague === employeeName;
      });
    },
    selectEmployee(employeeName) {
      this.$emit("selectEmployee", employeeName);
    }
  }
};
</script>

<style scoped>
.employee-list {
  width: 26vw;
  height: 100vh;
  background-color: rgba(26, 29, 36, 0.6);
  display: grid;
  grid-template-rows: 26vw 1fr;
}

img {
  height: 13vw;
  width: 13vw;
  margin: 0 auto;
  margin-top: 3rem;
  justify-self: flex-start;
}

ul {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  text-align: center;
  color: white;
}

li {
  padding: 0.5rem;
  user-select: none;
}
li:hover,
li.selected {
  background-color: #404146;
}

li.selected,
li.colleague {
  color: #3dd2fa;
}
</style>
