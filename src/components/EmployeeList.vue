<template>
  <div class="employee-list">
    <img src="@/assets/the-godfather.svg" alt="godfather logo" />
    <ul>
      <li>Name 1</li>
      <li>Name 2</li>
      <li>Name 3</li>
      <li>Name 4</li>
      <li>Name 5</li>
      <li>Name 6</li>
    </ul>
  </div>
</template>

<script>
export default {};
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
</style>
