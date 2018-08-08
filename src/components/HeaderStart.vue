<template>
  <div class="header">
    <h1 class="header__title">{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: "HeaderStart",
  data() {
    return {
      msg: "NewCrapker"
    };
  }
};
</script>

<!-- Аттрибут scoped добавляет стили конкретному компоненту -->
<style scoped>
h1 {
  font-weight: 400;
}
</style>
