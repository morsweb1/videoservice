<template>
<div class="container">
  <TopHeader />
  <div id="nav">
      <router-link to="/">Главная</router-link>
      <router-link to="/film">Фильмы</router-link>
      <router-link to="/serial">Сериалы</router-link>
    </div>
  <router-view/>
</div>
</template>

<script>
import TopHeader from '@/components/TopHeader'
export default {
  components: {
    TopHeader
  }
}

</script>

<style lang="less">
@font-face {
  font-family: 'RubikMedium';
  src: local('Rubik-Medium'), url('~@/assets/fonts/Rubik-Medium.ttf');
  font-weight: 500;
  font-style: normal;
}
@font-face {
  font-family: 'RubikRegular';
  src: local('Rubik-Regular'),  url('~@/assets/fonts/Rubik-Regular.ttf');
  font-weight: 400;
  font-style: normal;
}
body {
  margin: 0;
  padding: 0;
  
}
#app {
  font-family: 'RubikRegular';
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333333;
  font-size: 16px;
}
.container {
  max-width: 1180px;
  margin: 0 auto;
}
.btn {
  font-family: RubikMedium;
  font-weight: 500;
  font-size: 16px;
  padding: 10px 30px;
  background-color: #E5261E;
  color: #ffffff;
  border: none;
  outline: none;
  box-sizing: border-box;
  border-radius: 4px;
  cursor: pointer;
  &:hover {
    background-color: #CC221B;
  }
}
#nav {
  padding: 0 0 30px 0;

  a {
    font-family: RubikMedium;
    font-weight: 500;
    font-size: 28px;
    color: #333333;
    text-decoration: none;
    padding: 10px 0;
    margin: 0 12px;
    border-bottom: 2px solid transparent;
    transition: all .2s ease-in-out;
    &:hover {
      color: #E5261E;
      border-bottom: 2px solid #E5261E;
    }
    &.router-link-exact-active {
      color: #E5261E;
      border-bottom: 2px solid #E5261E;
    }
  }
}
.title-page {
  font-size: 26px;
  margin: 20px auto;
}
</style>
