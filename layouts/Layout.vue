<template>
  <div>
    <ParentLayout></ParentLayout>
    <Footer></Footer>
  </div>
</template>

<script>
import ParentLayout from '@parent-theme/layouts/Layout.vue'
import Footer from '@theme/components/Footer.vue'

export default {
  components: {
    ParentLayout,
    Footer
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

  color: var(--text-color) !important;
  background: var(--background) !important;
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

  .custom-block {
    &.tip,
    &.warning,
    &.danger { background-color: unset; color: unset; }
  }
}

a {color: #209ef6;
  &.sidebar-link { font-size: 0.85rem; color: var(--text-color);
    &:hover {color: #007dd4;}
    &.active {color: #209ef6; border-left-color: #209ef6;}
  }
  &[rel="noopener noreferrer"] {
    .icon {display: none;}
  }
  &.sidebar-heading { color: var(--text-color); }
}
.theme-default-content:not(.custom) a:hover {text-decoration: none;}
.theme-default-content code {color: var(--code); background: var(--code-background);}

.page {padding-left: 15rem;
  a {color: #209ef6; border-bottom: rgba(#209ef6, 0.2) 1px solid; transition: border 0.6s;
    &:hover {border-bottom-color: rgba(#209ef6, 0.6); transition: border 0.2s;}
  }
  a.header-anchor {transition: all 0.3s; padding-right: 0; margin-left: -1.2rem;
    &:hover {text-decoration: none;}
  }
  @media (max-width: 719px) {padding-left: 0; }
  &-nav .inner {border-top-color: var(--separator);}
  h2 {border-bottom-color: var(--separator);}
  th, td {border-color: var(--separator);}
  tr:nth-child(2n) {background: var(--table-alt-row);}
}

.navbar {border-bottom-color: var(--separator) !important; background: var(--background) !important;
  .links {background: transparent;}
  .logo {margin: 0;}
  .site-name {font-size: 1rem; display: none;}
}

.sidebar {border-right: 0 !important; overflow: hidden !important; width: 15rem !important; background: var(--background) !important;
  & > .sidebar-links {padding-bottom: 3rem; position: absolute; top: 0; bottom: 0; left: 0; width: 20rem; overflow-y: auto;
    & > li {width: 15rem;}
  }
  & > .sidebar-links > li > a.sidebar-link {border-bottom: 0; font-size: 0.85rem;}
  ul.sidebar-sub-headers {margin-bottom: 0.5rem;}
  @media (max-width: 719px) {box-shadow: none; top: 3.6rem;
    &-open .sidebar {box-shadow: 0 0 40px rgba(0,0,0,0.15);}
    .nav-links {position: absolute; bottom: 0; left: 0; right: 0; background: var(--background); z-index: 10;
      border-bottom: 0;
      .arrow {display: none;}
      .nav-dropdown {position: absolute; bottom: 100%; top: auto; background: var(--input);}
      .dropdown-wrapper.open .dropdown-title {margin: 0;
        &:hover {color: #209ef6;}
      }
    }
  }
}

.theme-default-content:not(.custom) {
  & > h1 {font-size: 2.5rem;}
}

.dropdown-wrapper {
  .dropdown-title {outline: none; line-height: normal; font-size: 0.85rem; color: var(--text-color);
    &:hover {color: #209ef6;}
  }
  .nav-dropdown {border: 0; box-shadow: 0 20px 40px rgba(0,0,0,0.15); background: var(--input);
    padding: 0.4rem;
    .dropdown-item a {transition: all 0.6s; padding: 0.5rem; border-radius: 4px; line-height: normal;
      &:hover {color: #209ef6; background: rgba(0,0,0,0.04); transition: all 0.2s;}
      &.router-link-active {color: #209ef6;
        &:after {display: none;}
      }
    }
  }
}

.search-box {
  input {border: 0; border-radius: 8px;
    background-color: var(--input);
    background-position: 0.8rem 0.6rem;
    background-repeat: no-repeat;
    background-size: 0.85rem; transition: all 0.3s; color: var(--input-text);
    &:focus {background-color: var(--input-focused);}
  }
  .suggestions {border: 0; box-shadow: 0 20px 40px rgba(0,0,0,0.15); background: var(--input);}
  .suggestion {padding: 0; padding: 0; background: transparent;
    a {display: block; border-radius: 4px; padding: 0.5rem; transition: all 0.6s; color: var(--text-color);}
    &:hover, &.focused {background: transparent;
      a {background: var(--input-focused); color: #209ef6; transition: all 0.2s;}
    }
  }
}
</style>