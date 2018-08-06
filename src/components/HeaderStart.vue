<template>
  <div class="header">
    <h1>{{ msg }}</h1>
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
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}

/* Skeleton Style */
</style>
