<template>
  <div class="card-item colorWhite watchCards">
    <h5 class="card-item-title"> {{card.title}} </h5>
    <div class="card-item-price">
       <span class="card-item-price-dolar">$</span><span class="card-item-price-price">{{ choice ? card.price.monthly : card.price.yearly }}</span><span class="card-item-price-choice">/ {{choice ? 'Monthly' : 'Yearly'}} </span>
    </div>
    <div class="card-item-video cardContent">
      <img class="card-item-video-arrow" src="@/static/Ok.svg" alt="okey">
      <span class="card-item-video-text"> {{card.video}} Video minutes </span>
    </div>
    <div class="card-item-languages cardContent">
      <img class="card-item-languages-arrow" src="@/static/Ok.svg" alt="okey">
      <span class="card-item-languages-text">Up to {{card.languages}} languages</span>
    </div>
    <div class="card-item-other1 cardContent">
      <img class="card-item-other1-arrow" src="@/static/Ok.svg" alt="okey" v-if="card.other1">
      <img class="card-item-other1-arrow" src="@/static/Error.svg" alt="okey" v-else>
      <span class="card-item-other1-text">Lorem ipsum dolor sit</span>
    </div>
    <div class="card-item-other2 cardContent">
      <img class="card-item-other2-arrow" src="@/static/Ok.svg" alt="okey" v-if="card.other2">
      <img class="card-item-other2-arrow" src="@/static/Error.svg" alt="okey" v-else>
      <span class="card-item-other2-text">Lorem ipsum dolor sit</span>
    </div>
    <div class="card-item-other3 cardContent">
      <img class="card-item-other3-arrow" src="@/static/Ok.svg" alt="okey" v-if="card.other3">
      <img class="card-item-other3-arrow" src="@/static/Error.svg" alt="okey" v-else>
      <span class="card-item-other3-text">Lorem ipsum dolor sit</span>
    </div>
    <button class="card-item-button">
        Try Now
    </button>
  </div>
</template>

<script>
export default {
  mounted () {
    const watchs = document.querySelectorAll(".watchCards");

    function checkSlide() {
      watchs.forEach(watch => {
        const slideInAt = (window.scrollY + window.innerHeight) - watch.offsetHeight / 2;
        const isHalfShown = slideInAt > watch.offsetTop;
        if (isHalfShown) {
          watch.classList.add('activeCard');
        } else {
          watch.classList.remove('activeCard');
        }
      });
    }
    window.addEventListener('scroll', checkSlide);
  },
  destroyed () {
    window.document.removeEventListener("scroll",  () => {});
  },
  props: {
    card: {
      type: Object,
      required: true,
    },
    choice: {
      type: Boolean,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
  .card-item {
    position: relative;
    border: 2px solid #89DBFF;
    box-sizing: border-box;
    border-radius: 1em;
    padding: 2em;
    width: 23.5%;

    opacity: 0;
    transform: translateY(50%) scale(1.5);;
    transition: all .7s;


    &-title {
      text-transform: uppercase;
      font-style: normal;
      font-weight: 800;
      font-size: 2em;
      line-height: 1em;
      background: -webkit-linear-gradient(#3DD1CA, #4C6BFF);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      text-align: center;
    }

    &-price {
      display: flex;
      justify-content: center;
      align-items: center;

      &-dolar {
        font-style: normal;
        font-weight: 600;
        font-size: 1em;
        line-height: 1.5em;
        margin: 0px .25em;
      }

      &-price {
        font-style: normal;
        font-weight: bold;
        font-size: 2.6em;
        line-height: 2em;
        margin: 0px .25em;
      }

      &-choice {
        font-style: normal;
        font-weight: 600;
        font-size: 1em;
        line-height: 1.5em;
        margin: 0px .25em;
      }
    }

    .cardContent {
      display: flex;
      align-items: center;
      line-height: 2em;

      img {
        width: 1.2em;
        height: 1.2em;
        margin-right: .5em;
      }
    }

    &-button {
      background: #89DBFF;
      border-radius: .5em;
      align-items: center;
      padding: .75em 1.5em;
      width: 100%;
      outline: none;
      border: none;
      text-transform: uppercase;
      font-style: normal;
      font-weight: bold;
      font-size: 1em;
      line-height: 1.5em;
      margin-top: 1.5em;
    }
  }

  .activeCard {
    opacity: 1;
    transform: translateY(0%) scale(1);
    transition: all .7s;
  }

@media (min-width: 993px) and (max-width: 1200px) {
  .card-item {
    padding: 1.5em;
  }
}

@media (max-width: 992px){
  .card-item {
    width: 95%;
  }
}

@media (max-width: 768px){
  
}

@media (max-width: 576px){

}

@media (max-width: 320px){

}
</style>