<template>
  <div class="Footer-floor">
    <button class="Footer-floor-button specialButton colorWhite">
      Subbedd
    </button>

    <div class="Footer-floor-links">
      <a class="floor-link" href="#">
        <img  src="@/static/Facebook.svg" alt="Facebook">
      </a>
      <a class="floor-link" href="#">
        <img src="@/static/twitter.svg" alt="Twitter">
      </a>
      <a class="floor-link" href="#">
        <img src="@/static/instagram.svg" alt="İnstagram">
      </a>
      <a class="floor-link" href="#">
        <img src="@/static/linkedin.svg" alt="Linkedin">
      </a>
    </div>

    <a href="https://lanista.com.tr" target="_blank" class="Footer-floor-lanista colorWhite">
      <span>made with</span>
      <img src="@/static/heart.svg" alt="Lanista heart">
      <span>by Lanista</span>
    </a>
    <a href="https://lanista.com.tr" target="_blank" class="Footer-floor-lanistaIcon">
      <img src="@/static/lanista.png" alt="Lanista">
    </a>

  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
.Footer-floor {
  margin-bottom: 1em;
  display: flex;
  justify-content: space-between;
  align-items: center;
  
  &-button {
    border-radius: 0;
  }

  &-lanista {
    text-decoration: none;
  }

  &-lanistaIcon {
    display: none;
  }
}


@media (max-width: 768px){
 .Footer-floor {
    &-lanista {
      display: none;
    }
    &-lanistaIcon {
      display: block;
      img {
        width: 6em;
      }
    }
  }
}
</style>