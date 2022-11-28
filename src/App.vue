<script setup>
import { ref } from "vue";
import Header from "./components/Header.vue";
import RecipeCard from "./components/RecipeCard.vue";
import Button from "./components/Button.vue";

const name = ref("");
const ingredients = ref("");
const instructions = ref("");
let recipes = ref([]);

function addRecipe() {
  recipes.value.push({
    name: name.value,
    ingredients: ingredients.value,
    instructions: instructions.value,
  });
}
</script>

<template>
  <div class="recipes-app">
    <Header></Header>

    <form>
      <div>
        <label>Dish Name</label>
        <input type="text" placeholder="Enter Dish Name" v-model="name" />
      </div>

      <div>
        <label>You Will Need</label>
        <input
          type="text"
          placeholder="Enter Ingredients"
          v-model="ingredients"
        />
      </div>

      <div>
        <label>Prepare</label>
        <textarea
          placeholder="Enter Instructions"
          v-model="instructions"
        ></textarea>
      </div>
      <Button
        type="button"
        class="submit"
        button-text="Submit Recipe"
        @click="addRecipe"
      ></Button>
    </form>
    <RecipeCard
      v-for="(recipe, index) in recipes"
      :key="index"
      :dish-name="recipe.name"
      :ingredients="recipe.ingredients"
      :prep-instructions="recipe.instructions"
    ></RecipeCard>
  </div>
</template>
<style scoped>
.recipes-app {
  background-color: #d1fbc2;
  border: 0.2rem solid #4ef111;
  height: auto;
  width: 75vh;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

input {
  width: 90%;
}

textarea {
  width: 90%;
  height: 7rem;
}

label {
  width: 90%;
}
</style>
