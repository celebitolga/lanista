<template>
  <div class="Footer-banner">
    <div class="Footer-banner-right">
      <h3 class="Footer-banner-right-title colorWhite">
        Subscribe for the latest news and updates !
      </h3>
      <p class="Footer-banner-right-text textGray">
        Join 10.950 subscribers and get latest news and updates to your inbox each month.
      </p>
      <form class="Footer-banner-right-form" @submit.prevent="">
        <input class="form-input" type="text" placeholder="example@gmail.com">
        <button class="form-button colorWhite" type="submit">Subscribe</button>
      </form>
    </div>
    <div class="Footer-banner-left">
      <div class="Footer-banner-left-holder">
        <img class="banner-image" src="@/static/footerbanner.svg" alt="Footer banner">
      </div>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.Footer-banner {
  background: #4C6BFF;
  border-radius: .5em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 2em 5em;
  margin: 7em 0 6.8em;

  &-right {

    &-title {
      font-size: 1em;
      font-style: normal;
      font-weight: 600;
      line-height: 1.5em;
      letter-spacing: 0em;
      text-align: left;
      margin-bottom: 1em;
    }

    &-text {
      font-size: .9em;
      font-style: normal;
      font-weight: 400;
      line-height: 1.25em;
      letter-spacing: 0em;
      text-align: left;
      margin-bottom: 1em;
    }

    &-form {
      position: relative;
      width: 100%;

      .form-input {
        padding: 1em 1em;
        background: #FFFFFF;
        border-radius: 8px;
        outline: none;
        border: 1px solid transparent;
        width: 80%;

        &:focus {
          border: 1px solid #5F24D9;
        }
      }
      .form-button {
        position: absolute;
        left: 63%;
        top: 50%;
        transform: translateY(-50%);
        padding: .5em 1.5em;
        background: #000C1B;
        border-radius: 4px;
        outline: none;
        border: none;
      }
    }
  }
}

@media (max-width: 992px){
  .Footer-banner {
    padding: 2em 3em;
    &-right {
      &-form {
        .form-button {
          left: 60%;
        }
      }
    }
  }
}

@media (max-width: 768px){
  .Footer-banner {
    padding: 1em 1em;
    background: #5F24D9;
    &-right {
      &-form {
        .form-button {
          left: 55%;
        }
      }
    }
  }
}

@media (max-width: 576px){
  .Footer-banner {
    margin: 3.75em 1em 4.75em;
    padding: 1em 1em;

    &-left {
      display: none;
      flex-basis: 0%;
    }
    &-right {
      flex-basis: 100%;
      &-form {
        position: static;
        display: flex;
        justify-content: space-between;
        align-items: center;

        width: 100%;
        .form-input {
          position: static;
          width: 100%;
          margin-right: 1em;
        }
        .form-button {
          position: static;
          padding: 1em 1em;
          transform: translateY(0%);
        }
      }
    }
  }
}
</style>