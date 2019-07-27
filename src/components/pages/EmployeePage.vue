<template>
  <div class="employee-page">
    <div class="background"></div>
    <img src="@/assets/images/header/godfather-header.jpg" alt="header image" />
    <div class="components-grid">
      <employee-list />
      <employee-detail />
    </div>
  </div>
</template>

<script>
import EmployeeList from "../EmployeeList";
import EmployeeDetail from "../EmployeeDetail";
import { getEmployeeData } from "../../api/employeeAPI/employeeAPI";
export default {
  name: "EmployeePage",
  components: {
    EmployeeList,
    EmployeeDetail
  },
  data() {
    return {
      employeeData: []
    };
  },
  mounted() {
    this.employeeData = getEmployeeData().employees;
    console.log(this.employeeData);
  }
};
</script>

<style scoped>
.employee-page {
  height: 100%;
  width: 100%;
  /* background-color: #2e2e36; */
}

.background {
  height: 100%;
  width: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background-color: #2e2e36;
  z-index: -2;
}

img {
  position: absolute;
  top: 0;
  left: 0;
  height: 35vh;
  width: 100vw;
  object-fit: none;
  z-index: -1;
}

.components-grid {
  display: grid;
  grid-template-columns: 26vw 1fr;
}
</style>
