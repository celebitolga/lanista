<template>
  <div>
    <section class="Section container">
      <div class="Section-content">
        <div class="Section-content-right watchs">
          <img src="@/static/Section_2.svg">
        </div>
        <div class="Section-content-left watchs">
          <div class="content-inside">
            <h4 class="content-inside-subtitle colorGreen">
              Cheaper translation service
            </h4>
            <h3 class="content-inside-title colorWhite">
              A video platform that provides subtitling service ?
            </h3>
            <p class="content-inside-paragraph colorGray">
              For even a cheaper translation service and a good chance to be viewed by internet users, you may opt to be on Subbedd video platform. We translate your video to up to 9 languages and you get to join our selection of videos in different categories !
            </p>
            <button class="content-inside-button specialButton colorWhite">
              See Pricing
            </button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>



<style lang="scss" scoped>
.Section {
  padding: 5.5em 0;
  overflow: hidden;

  &-content {
    display: flex;
    justify-content: space-between;
    align-items: center;

    &-left {
      order: 1;
      flex-basis: 45%;
      height: 300px;
      margin-right: 5%;

      opacity: 0;
      transform: translateX(-30%);
      transition: all .7s;
      
      .content-inside {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        align-content: space-between;

        &-subtitle {
          font-weight: bold;
          font-size: .8m;
          line-height: 20px;
          display: flex;
          justify-content: center;
          align-items: center;

          &::before {
            content: "";
            display: block;
            width: 15px;
            height: 3px;
            background: #50D38D;
            border-radius: 2px;
            margin-right: 5px;
          }
        }

        &-title {
          font-style: normal;
          font-weight: 800;
          font-size: 2em;
          line-height: 1.1em;
          margin: .5em 0;
        }

        &-paragraph {
          font-style: normal;
          font-weight: 400;
          font-size: 1em;
          line-height: 1.5em;
          margin-bottom: 1.4em;
        }
      }
    }

    &-right {
      order: 2;
      flex-basis: 55%;


      opacity: 0;
      transform: translateX(30%);
      transition: all .7s;
    }
  }
}

.active {
  opacity: 1;
  transform: translateX(0%) ;
  transition: all .7s;
}

@media (max-width: 992px){
  .Section {
    padding: 4.5em 0;

    &-content {
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-start;
      align-content: space-between;

      &-left {
        order: 1;
        flex-basis: 45%;
        margin: 0 0 2em;
      }

      &-right {
        order: 2;
        width: 100%;
        flex-basis: 55%;
      }
    }
  }
}
@media (max-width: 768px){
}

@media (max-width: 576px){
}

@media (max-width: 320px){
}
</style>