<template>
  <div class="backgroundWhite">
    <section class="Section container">
      <div class="Section-content">
        <div class="Section-content-right watchs">
          <img src="@/static/Section_1.svg">
        </div>
        <div class="Section-content-left watchs">
          <div class="content-inside">
            <h4 class="content-inside-subtitle colorGreen">Low-cost subtitling service</h4>
            <h3 class="content-inside-title colorWhite">What is Subbedd ?</h3>
            <p class="content-inside-paragraph colorGray">
              Subbedd is a low-cost, very accurate subtitling service. We use real translators to translate your videos for an affordable price. 
            </p>
            <p class="content-inside-paragraph colorGray">
              Most importantly, Subbedd is also a video browsing platform linking you with the rest of the world. You can be on Subbedd without even switching from a platform you already publish video in ! You just have to link it here and a click on Subbedd is a click on the platform you use !
            </p>
            <button class="content-inside-button specialButton colorWhite">Contact Us</button>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  mounted() {
    const watchs = document.querySelectorAll(".watchs");

    function checkSlide() {
      watchs.forEach(watch => {
        const slideInAt = (window.scrollY + window.innerHeight) - watch.offsetHeight / 2;
        const isHalfShown = slideInAt > watch.offsetTop;
        if (isHalfShown) {
          watch.classList.add('active');
        } else {
          watch.classList.remove('active');
        }
      });
    }
    window.addEventListener('scroll', checkSlide);
  },
  destroyed () {
    window.document.removeEventListener("scroll", () => {});
  },
}
</script>

<style lang="scss" scoped>
.Section {
  padding: 5.5em 0;
  overflow: hidden;

  &-content {
    display: flex;
    justify-content: space-between;
    align-items: center;

    &-left {
      flex-basis: 45%;
      height: 400px;
      margin-left: 5%;

      opacity: 0;
      transform: translateX(30%);
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
          line-height: 2em;
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
      flex-basis: 55%;


      opacity: 0;
      transform: translateX(-30%);
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