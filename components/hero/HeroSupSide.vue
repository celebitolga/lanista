<template>
  <div class="Hero-SupSide">
    <div class="Hero-SupSide-top">
      <div class="Hero-SupSide-top-left">
        <img class="" src="@/static/small.png" alt="Hero small">
        <img class="" src="@/static/small.png" alt="Hero small">
      </div>
      <div class="Hero-SupSide-top-right">
        <div class="Hero-SupSide-top-right-holder">
          <img class="imageBehind" :src="forGif.first" alt="Hero gif">
          <img class="imageAhead" src="@/static/blue.png" alt="Hero blue">
        </div>
      </div>
    </div>
    <div class="Hero-SupSide-bottom">
      <div class="Hero-SupSide-bottom-left">
        <div class="Hero-SupSide-bottom-left-holder">
          <img class="imageBehind" :src="forGif.second" alt="Hero gif">
          <img class="imageAhead" src="@/static/blue.png" alt="Hero blue">
        </div>
      </div>
      <div class="Hero-SupSide-bottom-right">
        <img class="" src="@/static/small.png" alt="Hero small">
        <img class="" src="@/static/small.png" alt="Hero small">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    forGif: Object,
  },
}
</script>

<style lang="scss" scoped>
.Hero-SupSide {
  width: 100%;
  &-top {
    display: flex;
    
    &-left {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      margin-right: 1em;
    }
    &-right {
      width: 100%;

      &-holder {
        position: relative;
        width: 100%;

        .imageBehind {
          position: absolute;
          transform: scale(.96);
          top: 2px;
          z-index: -1;
          width: 100%;
        }
        .imageAhead {
          width: 100%;
        }
      }
    }
  }
  &-bottom {
    display: flex;
    margin-top: 1em;

    &-right {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      margin-left: 1em;
    }
    &-left {
      width: 100%;

      &-holder {
        position: relative;
        width: 100%;

        .imageBehind {
          position: absolute;
          transform: scale(.96);
          top: 2px;
          z-index: -1;
          width: 100%;
        }
        .imageAhead {
          width: 100%;
        }
      }
    }
  }
}

@media (min-width: 993px) and (max-width: 1200px) {
  .Hero-SupSide {
    &-top {
      
      &-left {
        img {
          width: 110%;
          margin-bottom: 1em;
        }
      }
      &-right {
        width: 80%;
      }
    }
    &-bottom {

      &-right {
        img {
          width: 110%;
          margin-bottom: 1em;
        }
      }
      &-left {
        width: 80%;
      }
    }
  }
}
</style>