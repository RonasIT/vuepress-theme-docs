<template>
  <footer class="footer">
    <div class="footer-content">
      © 2020 <a href="https://www.ronasit.com" target="_blank">Ronas IT</a>
    </div>
  </footer>
</template> 

<style lang="scss">
  .footer {width: 15rem; position: fixed; left: 0; bottom: 0; padding: 0.7rem 1.5rem; z-index: 10;
  box-sizing: border-box;
  background: var(--background);
    &-content {max-width: 740px; margin: 0 auto; color: #476582; font-size: 0.85rem;}
    a {color: #476582; border-bottom: transparent 1px solid; font-weight: normal; transition: all 0.6s;
      &:hover {border-bottom-color: rgba(#209ef6, 0.2); transition: all 0.2s; color: #007dd4;}
    }
    @media (max-width: 719px) {margin-left: 0; position: static;}
  }
</style>