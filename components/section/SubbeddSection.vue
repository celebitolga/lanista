<template>
  <div>
    <section class="Section container">
      <div class="Section-content">
        <div class="Section-content-right watchs">
          <div class="Section-content-right-up">
            <div class="up-item marginRight marginBottom">
              <img src="@/static/Upitem1.svg" alt="" class="up-item-image">
              <h5 class="up-item-title colorWhite">No burden on your budget</h5>
              <p class="up-item-text colorGray">To reach talented creators with different budgets, our offers are far below the market price.</p>
            </div>
            <div class="up-item">
              <img src="@/static/Upitem2.svg" alt="" class="up-item-image">
              <h5 class="up-item-title colorWhite">Don’t lose your revenue</h5>
              <p class="up-item-text colorGray">Videos are linked ! Every view here is also a view on your video</p>
            </div>
          </div>
          <div class="Section-content-right-down">
            <div class="down-item marginRight marginBottom">
              <img src="@/static/Downitem1.svg" alt="" class="down-item-image">
              <h5 class="down-item-title colorWhite">Reach out everyone</h5>
              <p class="down-item-text colorGray">No more worrying about algorithms to be seen.</p>
            </div>
            <div class="down-item">
              <img src="@/static/Downitem2.svg" alt="" class="down-item-image">
              <h5 class="down-item-title colorWhite">Variety of Options</h5>
              <p class="down-item-text colorGray">Our offers don’t suit you ? Our prices and services are adjustable to your need.</p>
            </div>
          </div>
        </div>
        <div class="Section-content-left watchs">
          <div class="content-inside">
            <h3 class="content-inside-title colorWhite">
              What is Subbedd ?
            </h3>
            <p class="content-inside-paragraph colorGray">
              Subbedd is a low-cost, very accurate subtitling service. 
              We use real translators to translate your videos for an affordable price.
            </p>
            <p class="content-inside-paragraph colorGray">
              Most importantly, Subbedd is also a video browsing platform linking you with the rest of the world. 
              You can be on Subbedd without even switching from the platform you already publish video in ! 
              You just have to link it here and a click on Subbedd is a click on the platform you use !
            </p>
            <a class="content-inside-link" href="#">
              <span class="content-inside-link-text">See pricing options</span>
              <img src="@/static/Arrow.svg" alt="">
            </a>
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
      flex-basis: 32%;
      align-self: flex-start;

      opacity: 0;
      transform: translateX(-30%);
      transition: all .7s;
      
      .content-inside {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        align-content: space-between;

        &-title {
          font-style: normal;
          font-weight: 800;
          font-size: 1.9em;
          line-height: 1.1em;
          margin: .5em 0;
          display: flex;
          justify-content: center;
          align-items: center;

          &::before {
            content: "";
            display: block;
            width: 24px;
            height: 4px;
            background: #fff;
            border-radius: 2px;
            margin-right: .5em;
          }
        }

        &-paragraph {
          font-style: normal;
          font-weight: 400;
          font-size: 1em;
          line-height: 1.5em;
          margin-bottom: 1.4em;
        }

        &-link {
          display: flex;
          justify-content: flex-start;
          align-items: center;
          text-decoration: none;
          color: #89DBFF;
          font-size: .8em;
          font-weight: bold;
          line-height: 20px;
          width: 100%;
          &-text {
            margin-right: .5em;
          }
        }
      }
    }

    &-right {
      order: 2;
      flex-basis: 60%;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      font-size: 1em;
      line-height: 1.5em;

      opacity: 0;
      transform: translateX(30%);
      transition: all .7s;

      &-up {
        display: flex;
        justify-content: center;
        align-items: flex-start;
        margin-bottom: 3em;
        .up-item {
          width: 50%;

          &-image {
            margin-bottom: 1.5em;
          }

          &-title {
            margin-bottom: 1.5em;
          }
        }
        .marginRight {
          margin-right: 5em;
        }
      }

      &-down {
        display: flex;

        .down-item {
          width: 50%;

          &-image {
            margin-bottom: 1.5em;
          }

          &-title {
            margin-bottom: 1.5em;
          }
        }
        .marginRight {
          margin-right: 5em;
        }
      }
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
        margin: 0 0 2em;

        .content-inside-title {
          &::before {
            display: none;
          }
        }

        .content-inside-paragraph {
          display: none;
        }
        .content-inside-link {
          display: none;
        }
      }

      &-right {
        order: 2;
      }
    }
  }
}
@media (max-width: 768px){
  .Section {

    &-content {

      &-right {
        &-up {
          flex-direction: column;

          .up-item {
            width: 100%;
          }
        }
        .marginRight {
          margin-right: 0;
        }
        .marginBottom {
          margin-bottom: .5em;
        }

        &-down {
          flex-direction: column;
          
          .down-item {
            width: 100%;
          }
        }
        .marginRight {
          margin-right: 0;
        }
        .marginBottom {
          margin-bottom: 1.5em;
        }
      }
    }
  }
}

</style>