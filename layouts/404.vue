<template>
  <div class="page-not-found">
    <NotFoundLogo />
    <p><strong>404!</strong> Page no found.</p>
  </div>
</template>

<script>
import NotFoundLogo from '@theme/components/NotFoundLogo.vue'

export default {
  components: {
    NotFoundLogo
  }
}
</script>

<style lang="scss">
html, body {
  --text-color: #000;
  --background: #fff;
  --separator: #eaecef;
  --input: #f8f8f8;
  --table-alt-row: #f8f8f8;
  --input-focused: #f2f2f2;
  --input-text: #000;
  --code: #476582;
  --code-background: rgba(27,31,35,0.05);

  color: var(--text-color);
  background: var(--background);
}

@media (prefers-color-scheme: dark) { 
  html, body {--text-color: #B2C3D4; 
    --background: #18222D;
    --separator: #22303F;
    --input: #22303F;
    --table-alt-row: #1B2632;
    --input-focused: #2F4256;
    --input-text: #B2C3D4;
    --code: #7693B1;
    --code-background: #22303F;
  }
} 

.page-not-found {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: center;
}
</style>