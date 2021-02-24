<template>
  <div class="Hero-slogan">
    <h2 class="Hero-slogan-title">
      Discover the world for free !
    </h2>
    <p class="Hero-slogan-text colorWhite">
      Browse videos globally to watch in your language.
    </p>
  </div>
</template>
<style lang="scss" scoped>
.Hero-slogan {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 0 78px;

  &-title {
    color: #50D38D;
    text-transform: uppercase;
    font-style: normal;
    font-weight: 800;
    font-size: 1em;
    line-height: 24px;
    margin-bottom: 1.5em;
    text-align: center;
  }

  &-text {
    font-style: normal;
    font-weight: 800;
    font-size: 1.8em;
    line-height: 32px;
    text-align: center;
  }
}
</style>