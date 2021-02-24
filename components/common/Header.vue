<template>
  <header class="Header">
    <div class="Header-left">
      <h1 class="Header-left-title">Subbedd</h1>
    </div>
    <nav class="Header-right">
      <ul class="nav-items colorWhite">
        <li class="nav-items-item">
          What is Subbedd ?
        </li>
        <li class="nav-items-item">
          How ?
        </li>
        <li class="nav-items-item">
          Pricing
        </li>
      </ul>
      <button class="Header-right-button specialButton colorWhite">Contact Us</button>
    </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.Header {
  max-width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 72px;
  &-left {
    &-title {
      font-style: normal;
      font-weight: 800;
      line-height: 24px;
      text-transform: uppercase;
      color: #5F24D9;
      font-size: 1.5em;
      cursor: pointer;
    }
  }

  &-right {
    display: flex;
    justify-content: center;
    align-items: center;

    .nav-items {
      display: flex;
      justify-content: center;
      align-items: center;

      &-item {
        cursor: pointer;
        font-size: 1em;
        font-weight: 400;
        margin-right: 16px;
      }
    }
    &-button {

    }
  }
}

@media (max-width: 992px){
  .Header {
    padding: 0 20px;
    .nav-items {
      display: none;
    }
  }
}
@media (max-width: 768px){
  .Header {
    padding: 0 10px;
  }
}

@media (max-width: 576px){
  .Header {
    padding: 0 3px;
  }
}

@media (max-width: 320px){
  
}
</style>