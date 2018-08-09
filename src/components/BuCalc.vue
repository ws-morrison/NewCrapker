<template>
  <div class='bu-calc'>
    <h2 class='bu-calc__title'>{{ msg }}</h2>
    <input class='bu-calc__input' type='number' placeholder='Углеводов на 100гр продукта' v-model='carbs' autofocus>
    <input class='bu-calc__input' type='number' placeholder='Масса нетто' v-model='nett'>
    <div class='bu-calc__output'>
      <span class='bu-calc__result'>{{ resCU.toFixed(1) }} ХЕ</span>
    </div>

    <!--https://thenounproject.com/search/?q=reset&i=415758 -->
    <button class='bu-calc__reset' v-on:click='resetCalc'>
      <!-- <svg xmlns:dc='http://purl.org/dc/elements/1.1/' xmlns:cc='http://creativecommons.org/ns#' xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'
        xmlns:svg='http://www.w3.org/2000/svg' xmlns='http://www.w3.org/2000/svg' xmlns:sodipodi='http://sodipodi.sourceforge.net/DTD/sodipodi-0.dtd'
        xmlns:inkscape='http://www.inkscape.org/namespaces/inkscape' version='1.1' x='0px' y='0px' viewBox='0 0 100 125' width='25px'
        height='25px'>
        <g transform='translate(0,-952.36218)'>
          <path style='text-indent:0;text-transform:none;direction:ltr;block-progression:tb;baseline-shift:baseline;color:#000000;enable-background:accumulate;'
            d='m 12.779718,963.39615 a 1.9985068,1.9985283 0 0 0 -1.186494,3.43463 l 35.563621,35.56402 -35.563621,35.5328 a 1.9985068,1.9985283 0 1 0 2.810119,2.8413 l 35.563621,-35.5639 35.56362,35.5639 a 1.9985068,1.9985283 0 1 0 2.810119,-2.8413 l -73.93736,-73.9382 a 1.9985068,1.9985283 0 0 0 -1.623625,-0.59325 z m 73.906137,0 a 1.9985068,1.9985283 0 0 0 -1.155271,0.59325 l -30.973759,30.97409 a 1.9985068,1.9985283 0 1 0 2.810119,2.84138 l 30.973759,-30.97409 a 1.9985068,1.9985283 0 0 0 -1.654848,-3.43463 z'
            fill='#000000' fill-opacity='1' stroke='none' marker='none' visibility='visible' display='inline' overflow='visible'
          />
        </g>
      </svg> -->
    </button>

  </div>
</template>

<script>
export default {
  name: 'BuCalc',
  data () {
    return {
      msg: 'Калькулятор ХЕ',

      // Связывает данные с одноимёнными v-model
      carbs: '',
      nett: ''
    }
  },
  computed: {
    // Формула подсчёта ХЕ
    resCU: function () {
      return (this.carbs / 100) * (this.nett / 10)
    }
  },
  methods: {
    // Сброс
    resetCalc: function () {
      this.carbs = ''
      this.nett = ''
    }
  }
}

</script>

<!-- Аттрибут scoped добавляет стили конкретному компоненту -->
<style scoped>
  .bu-calc__title {
    font-weight: 300;
  }

  .bu-calc {
    width: 320px;
    margin: 0 auto;
    padding: 0;
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
    width: 55%;
    padding: 10px;
    margin: 0 auto;
    border: 1px solid #000000;
    border-radius: 4px;
    background: none;
  }

  .bu-calc__reset {
    position: relative;
    left: 259px;
    top: -52px;
    width: 24px;
    height: 24px;
    background-color: inherit;
    background-image: url('../assets/reset.svg');
    background-repeat: no-repeat;
    background-position: 2px 2px;
    border-radius: 50%;
    border: none;
    padding: 0;
    margin: 0;
  }

</style>
