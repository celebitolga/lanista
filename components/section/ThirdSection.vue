<template>
  <div class="backgroundWhite">
    <section class="Section container">
      <div class="Section-content">
        <div class="Section-content-right watchs">
          <img src="@/static/Section_3.svg">
        </div>
        <div class="Section-content-left watchs">
          <div class="content-inside">
            <h3 class="content-inside-title colorWhite">How will Subbedd access my video and provide subtitling ?</h3>
            <h4 class="content-inside-subtitle colorGreen">
              That's easy. There are two ways:
            </h4>
            <ul class="content-inside-list colorGray">
              <li class="content-inside-list-item">
                <span class="content-inside-list-item-block"></span>
                <p class="content-inside-list-item-paragraph">
                If you already uploaded your content on any other video platform, 
                just share the video link with us. 
                Your video or channel will keep gaining followers and views on that platform via Subbedd.
                </p>
              </li>
              <li class="content-inside-list-item">
                <span class="content-inside-list-item-block"></span>
                <p class="content-inside-list-item-paragraph">
                  We are getting so excited when getting new videos. 
                  Share your video via <span class="colorYellow">[we need to provide a way of sending here]</span>
                   with us and let us do the rest!
                </p>
              </li>
            </ul>
            <form @click.prevent="" class="content-inside-form">
              <input type="text" class="content-inside-form-input" placeholder="exaple@mail.com">
              <button class="content-inside-form-button specialButton colorWhite" type="submit">Subscribe</button>
            </form>
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
          margin: 0 0 .5em;

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
          margin: 0 0 .5em;
        }

        &-list {
          &-item {
            margin: 24px 0px;
            display: flex;

            &-block {
              background: #50D38D;
              border-radius: 2px;
              width: 10px;
              height: 4px;
              padding: 3px;
            }

            &-paragraph {
              margin-left: 20px;
            }
          }
        }

        &-form {
          width: 100%;
          display: flex;
          justify-content: space-between;
          align-items: center;

          &-input {
            border: 1px solid transparent;
            outline: none;
            background: #FFFFFF;
            padding: .5em .75em;
            border-radius: 5px;
            width: 100%;
            padding: .6em .5em;
            margin-right: 1em;

            &:focus {
              border: 1px solid #5F24D9;
            }
          }
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