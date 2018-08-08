<template>
  <div class="bu-calc">
    <h2 class="bu-calc__title">{{ msg }}</h2>
    <input class="bu-calc__input" type="number" placeholder="Углеводов на 100гр продукта" v-model="carbs">
    <input class="bu-calc__input" type="number" placeholder="Масса нетто" v-model="nett">
    <div class="bu-calc__output">
    <span class="bu-calc__result">{{ resCU.toFixed(1) }} ХЕ</span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "BuCalc",
    data() {
      return {
        msg: "Калькулятор хлебных единиц",

        // Связывает данные с одноимёнными v-model
        carbs: "",
        nett: ""
      };
    },
    computed: {
      // Формула подсчёта ХЕ
      resCU: function () {
        return (this.carbs / 100) * (this.nett / 10);
      }
    }
  };

</script>

<!-- Аттрибут scoped добавляет стили конкретному компоненту -->
<style scoped>
  .bu-calc__title {
    font-weight: 300;
  }

  .bu-calc {
    margin: 0 auto;
    width: 380px;
    display: flex;
    flex-direction: column;
  }

  .bu-calc__input {
    border: none;
    border-bottom: 1px solid #afafaf;
    padding: 15px;
    margin-bottom: 15px;
  }

  .bu-calc__output {
    font-size: 22px;
    font-weight: 500;
    width: 75%;
    padding: 10px;
    margin: 0 auto;
    border: 1px solid #000000;
    border-radius: 4px;
    background: none;
  }

</style>
