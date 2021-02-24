<template>
  <div>
    <Header class="container"/>

    <Nuxt />
  </div>
</template>

<script>
import Header from '@/components/common/Header';

export default {
  components: {
    Header,
  },  
}
</script>

<style lang="scss">
html {
  font-family: 'Nunito', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  background: #000C1B;
}

.container {
  max-width: 1148px;
  margin-left: auto;
  margin-right: auto;
  //width: calc(100% - 20px);
}

.backgroundWhite {
  background: rgba(255, 255, 255, 0.1);
}

.colorWhite {
  color: #fff;
}

.colorGray {
  color: rgba(255, 255, 255, 0.8);
}

.colorGreen {
  color: #50D38D;
}

.specialButton {
  cursor: pointer;
  background-color: #5F24D9;
  border-radius: 7px;
  padding: 8px 24px;
  font-size: 1em;
  outline: none;
  border: none;
  transition: all 300ms;
  font-style: normal;
  font-weight: 600;
  line-height: 24px;
  
  &:hover {
    background-color: #2f0681;
  }
}


@media (min-width: 993px) and (max-width: 1200px) {
  html {
    font-size: 15px;
  }
  .container {
    max-width: 960px;
  }
}

@media (max-width: 992px){
  html {
    font-size: 15px;
  }
  .container {
    max-width: 720px;
  }
}
@media (max-width: 768px){
  html {
    font-size: 14px;
  }
  .container {
    max-width: 540px;
  }
}

@media (max-width: 576px){
  html {
    font-size: 13px;
  }
  .container {
    margin: 0 .8em;
  }
}

@media (max-width: 320px){
  html {
    font-size: 12px;
  }
  .container {
    margin: 0 .5em;
  }
}

</style>
