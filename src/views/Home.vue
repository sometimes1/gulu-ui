<template>
  <div>
    <div class="topnavAndBanner">
      <Topnav />
      <div class="banner">
        <h1>轱辘UI</h1>
        <h2>一个基于Vue3 UI 框架</h2>
        <p class="actions">
          <a href="https://github.com">GitHub</a>
          <router-link to="/doc">开始</router-link>
        </p>
      </div>
    </div>
  </div>
  <div class="features">
    <ul>
      <li>
        <svg>
          <use xlink:href="#icon-Vue" />
        </svg>
        <h3>基于 Vue 3</h3>
        <p>骄傲地使用了 Vue 3 Composition API</p>
      </li>
      <li>
        <svg>
          <use xlink:href="#icon-ts" />
        </svg>
        <h3>基于 TypeScript</h3>
        <p>源代码采用 TypeScript 书写（非严格检查）</p>
      </li>
      <li>
        <svg>
          <use xlink:href="#icon-light" />
        </svg>
        <h3>代码易读</h3>
        <p>每个组件的源代码都极其简洁</p>
      </li>
    </ul>
  </div>
</template>
<script lang="ts">
import Topnav from '../components/Topnav.vue'
export default {
  components: {
    Topnav
  }
}
</script>
<style lang="scss" scoped>
$yellow: #ffca39;
$border-radius: 4px;
$blue: #000046;
.topnavAndBanner {
  background: rgba(47, 47, 47, 1);
  // background: rgb(108, 105, 105);
  // background: linear-gradient(
  //   142deg,
  //   rgba(108, 105, 105, 0.7850534539473684) 0%,
  //   rgba(48, 48, 48, 1) 100%
  // );
  // border-bottom-left-radius:50% 80px;
  // border-bottom-right-radius:50% 80px;
  clip-path: ellipse(80% 60% at 50% 40%);
}
.features {
  margin: 64px auto;
  @media (min-width: 800px) {
    width: 800px;
  }
  @media (min-width: 1200px) {
    width: 1200px;
  }
  > ul {
    display: flex;
    flex-wrap: wrap;
    > li {
      width: 400px;
      margin: 16px 0;
      display: grid;
      justify-content: start;
      align-content: space-between;
      grid-template-areas:
        'icon title'
        'icon text';
      grid-template-columns: 80px auto;
      grid-template-rows: 1fr auto;
      > svg {
        grid-area: icon;
        width: 64px;
        height: 64px;
      }
      > h3 {
        grid-area: title;
        font-size: 28px;
      }
      > p {
        grid-area: text;
      }
    }
  }
}
.banner {
  color: white;
  padding: 100px 0;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  > .actions {
    padding: 8px 0;
    a {
      margin: 0 8px;
      color: $blue;
      background: $yellow;
      display: inline-block;
      padding: 8px 24px;
      border-radius: $border-radius;
      &:hover {
        text-decoration: none;
      }
    }
  }
}
</style>