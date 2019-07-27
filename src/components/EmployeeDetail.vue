<template>
  <div class="employee-detail">
    <div class="profile-grid">
      <img
        src="@/assets/images/profile-pics/vito-corleone.jpg"
        alt="profile picture"
        class="profile-image"
      />

      <div class="employee-popularity">
        <h1 class="employee-name">Vito Corleone</h1>
        <div class="popularity">
          <span>Popularity</span>
          <input
            type="range"
            min="1"
            max="5"
            value="2"
            class="slider"
            id="myRange"
          />
        </div>
      </div>
      <div class="biography">
        <h3>Biography</h3>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Aliquam
        quaerat reiciendis magnam, maiores molestias cumque fugiat placeat
        consequatur eum magni eligendi sint aliquid minus fuga porro iusto qui
        voluptas nulla? Voluptas sint cum veniam laboriosam deserunt. Modi
        dolorem neque nihil quaerat eius deleniti, illum rerum commodi et quod
        perspiciatis delectus? Id blanditiis laudantium dicta ad. Voluptas
        doloribus possimus quis! Quasi deserunt blanditiis similique animi modi
        sit tempora incidunt vitae, sequi illum. Exercitationem voluptates fuga
        maiores adipisci nihil. Magni hic laboriosam assumenda asperiores vero
        consequuntur esse numquam repellat illum obcaecati porro reiciendis
        eveniet explicabo aperiam repudiandae tempora atque, doloremque,
        corrupti architecto.
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.profile-grid {
  height: 100vh;
  margin-top: 20%;
  margin-right: 5%;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr 1fr 1fr;
  grid-template-areas:
    "p pop pop pop"
    ". bio bio bio"
    ". bio bio bio"
    ". bio bio bio";
  justify-items: center;
  color: white;
}

.profile-image {
  padding: 0 auto;
  grid-area: p;
  max-height: 90%;
  border: 2px solid #5a595e;
  border-radius: 3.5%;
}

.employee-name {
  grid-area: n;
  margin: 0;
  font-weight: 400;
  font-size: 3rem;
}

.employee-popularity {
  grid-area: pop;
  justify-self: start;
  width: 100%;
}

.popularity {
  width: 100%;
  display: flex;
  margin-top: 3rem;
}

.popularity > span {
  display: inline-block;
  font-size: 2rem;
}

.popularity > input {
  width: 100%;
  margin-top: 1rem;
  margin-left: 2rem;
}

.slider {
  -webkit-appearance: none;
  width: 100%;
  height: 0.3rem;
  background: #1a1d24;
  border-radius: 2px;
  outline: none;
}

.slider:hover {
  opacity: 1;
}

.slider::-webkit-slider-thumb {
  -webkit-appearance: none;
  appearance: none;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  background: white;
  cursor: pointer;
}

.slider::-moz-range-thumb {
  width: 25px;
  height: 25px;
  background: white;
  cursor: pointer;
}

.biography {
  grid-area: bio;
  background-color: #1a1d24;
  padding: 1rem;
  border-radius: 1%;
}

.biography > h3 {
  font-size: 2rem;
  font-weight: 400;
}
</style>
