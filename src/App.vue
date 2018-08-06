<template>
  <div id="app">
    <HeaderStart/>
  </div>
</template>

<script>
import HeaderStart from "./components/HeaderStart";

export default {
  name: "App",
  components: {
    HeaderStart
  }
};
</script>

<style scoped>
#app {
  font-family: "Montserrat", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* Skeleton styles */
.button,
button,
input[type="submit"],
input[type="reset"],
input[type="button"] {
  display: inline-block;
  height: 38px;
  padding: 0 30px;
  color: #555;
  text-align: center;
  font-size: 11px;
  font-weight: 600;
  line-height: 38px;
  letter-spacing: 0.1rem;
  text-transform: uppercase;
  text-decoration: none;
  white-space: nowrap;
  background-color: transparent;
  border-radius: 4px;
  border: 1px solid #bbb;
  cursor: pointer;
  box-sizing: border-box;
}
.button:hover,
button:hover,
input[type="submit"]:hover,
input[type="reset"]:hover,
input[type="button"]:hover,
.button:focus,
button:focus,
input[type="submit"]:focus,
input[type="reset"]:focus,
input[type="button"]:focus {
  color: #333;
  border-color: #888;
  outline: 0;
}
.button.button-primary,
button.button-primary,
input[type="submit"].button-primary,
input[type="reset"].button-primary,
input[type="button"].button-primary {
  color: #fff;
  background-color: #33c3f0;
  border-color: #33c3f0;
}
.button.button-primary:hover,
button.button-primary:hover,
input[type="submit"].button-primary:hover,
input[type="reset"].button-primary:hover,
input[type="button"].button-primary:hover,
.button.button-primary:focus,
button.button-primary:focus,
input[type="submit"].button-primary:focus,
input[type="reset"].button-primary:focus,
input[type="button"].button-primary:focus {
  color: #fff;
  background-color: #1eaedb;
  border-color: #1eaedb;
}

h1,
h2,
h3,
h4,
h5,
h6 {
  margin-top: 0;
  margin-bottom: 2rem;
  font-weight: 300;
}
h1 {
  font-size: 4rem;
  line-height: 1.2;
  letter-spacing: -0.1rem;
}
h2 {
  font-size: 3.6rem;
  line-height: 1.25;
  letter-spacing: -0.1rem;
}
h3 {
  font-size: 3rem;
  line-height: 1.3;
  letter-spacing: -0.1rem;
}
h4 {
  font-size: 2.4rem;
  line-height: 1.35;
  letter-spacing: -0.08rem;
}
h5 {
  font-size: 1.8rem;
  line-height: 1.5;
  letter-spacing: -0.05rem;
}
h6 {
  font-size: 1.5rem;
  line-height: 1.6;
  letter-spacing: 0;
}
</style>
