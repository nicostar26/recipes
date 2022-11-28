<script setup>
const props = defineProps({
  buttonText: String,
});
</script>

<template>
  <button>{{ buttonText }}</button>
</template>

<style scoped>
button {
  width: 8rem;
  height: 3rem;
  font-weight: bold;
  margin: 1rem;
  background-color: color;
}

.delete {
  background-color: #f49699;
  border: 0.2rem #ea372c solid;
  color: white;
  border-radius: 10px;
  font-weight: bold;
}

.edit {
  background-color: #edf98b;
  border: 0.2rem #f1f50a solid;
  border-radius: 10px;
  font-weight: bold;
}

.submit {
  background-color: #cd5ff6;
  color: white;
  border: 0.2rem white solid;
  border-radius: 10px;
  font-weight: bold;
  margin-left: 0px;
}
</style>
