<template>
  <div class="backgroundWhite">
    <section class="Section container">
      <div class="Section-content">
        <h2 class="Section-content-title colorWhite">Our offers for in Platfom Service</h2>

        <div class="Section-content-buttons">
          <button @click="selected(true)" class="Section-content-buttons-default" :class="{'buttonSelected': choice}">Month</button>
          <button @click="selected(false)" class="Section-content-buttons-default" :class="{'buttonSelected': !choice}">Year</button>
        </div>

        <Cards class="Section-content-cards" :cards="cards" :choice="choice"/>
        
      </div>
    </section>
  </div>
</template>

<script>
import Cards from '@/components/section/Cards';
export default {
  data() {
    return {
      choice: true,
    }
  },
  props: {
    cards: {
      type: Array,
      required: true,
    },
  },
  components: {
    Cards,
  },
  methods: {
    selected(selected) {
      this.choice = selected;
    },
  },
}
</script>

<style lang="scss" scoped>
.Section {
  padding: 5em 0;

  &-content {
    display: flex;
    flex-direction: column;
    align-items: center;

    &-title {
      font-style: normal;
      font-weight: 800;
      font-size: 2em;
      line-height: 2em;
      text-align: center;
      margin-bottom: .5em;
    }

    &-buttons {
      text-align: center;
      background: #A6A9B6;
      border-radius: 4px;
      padding: 4px;
      margin-bottom: 3em;

      &-default {
        color: #6024d996;
        background-color: transparent;
        border-radius: 4px;
        font-style: normal;
        font-weight: bold;
        font-size: .8em;
        line-height: 1.4em;
        outline: none;
        border: none;
        padding: .25em .75em;

        &:hover {
          box-shadow: 0px 0px 20px rgba(0, 0, 0, 1);
        }
      }
    }

    &-cards {
      width: 100%;
      display: flex;
      justify-content: space-between;
      //align-items: center;
      
    }
  }
}
.buttonSelected {
  background: #FFFFFF;
  box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.06);
  color: #5F24D9;
}

@media (max-width: 992px){

}
@media (max-width: 768px){
}

@media (max-width: 576px){
}

@media (max-width: 320px){
}
</style>