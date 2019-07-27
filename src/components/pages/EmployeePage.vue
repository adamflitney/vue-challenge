<template>
  <div class="employee-page">
    <employee-list />
    <employee-detail />
  </div>
</template>

<script>
import EmployeeList from "../EmployeeList";
import EmployeeDetail from "../EmployeeDetail";
export default {
  name: "EmployeePage",
  components: {
    EmployeeList,
    EmployeeDetail
  }
};
</script>

<style></style>
