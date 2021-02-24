<template>
  <section class="Hero container">
    <HeroSlogan />

    <div class="Hero-content">
      <HeroSupSide class="Hero-content-supside" :forGif="{first: 'gif_01.gif', second: 'gif_02.gif' }"/>
      
      <HeroMiddleVideo class="Hero-content-middlevideo"/>
      
      <HeroSupSide class="Hero-content-supside" :forGif="{first: 'gif_03.gif', second: 'gif_04.gif' }"/>
    </div>

  </section>
</template>

<style lang="scss" scoped>
.Hero {
  padding: 3em 0 5em;

  .Hero-content {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;

    &-supside {
      width: 24%;
    }

    &-middlevideo {
      display: flex;
      justify-content: center;
      align-items: center;
      width: 50%;
      height: 390px;
    }
  }
}

@media (min-width: 993px) and (max-width: 1200px) {
  .Hero {
    .Hero-content {
      &-supside {
        width: 24%;
      }

      &-middlevideo {
        width: 48%;
        height: 340px;
      }
    }
  }
}

@media (max-width: 992px){
  .Hero {
    .Hero-content {
      &-supside {
        display: none;
      }

      &-middlevideo {
        width: 100%;
        height: 450px;
      }
    }
  }
}
</style>