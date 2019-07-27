<template>
  <div class="employee-page">
    <employee-list />
    <employee-detail />
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

<style></style>
