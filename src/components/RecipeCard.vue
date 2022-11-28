<script setup>
import Button from "./Button.vue";
defineProps({
  dishName: "",
  ingredients: "",
  prepInstructions: "",
});
</script>
<template>
  <div class="card-wrapper">
    <div class="dish-name">
      <h3>Dish Name:</h3>
      <span>{{ dishName }}</span>
    </div>
    <div class="ingredients">
      <h3>Ingredients:</h3>
      <ul>
        <li>{{ ingredients }}</li>
      </ul>
    </div>
    <div class="prep">
      <h3>Preparation Instructions:</h3>
      <p>{{ prepInstructions }}</p>
    </div>
    <div class="buttons">
      <Button button-text="Edit" class="edit"></Button>
      <Button button-text="Delete" class="delete"></Button>
    </div>
  </div>
</template>
<style scoped>
.card-wrapper {
  background-color: #ecc2fb;
  border: 0.2rem solid #cd5ff6;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  width: 75%;
  padding: 2rem;
  margin: 2rem;
}

.dish-name {
  display: flex;
  align-items: center;
}
.ingredients {
  display: flex;
}
h3 {
  margin-right: 1rem;
}

p {
  margin-right: 1rem;
}

.buttons {
  display: flex;
}
</style>
