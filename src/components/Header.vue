<template>
  <div class='header-container'>
    <nav class='nav-container'>
      <div class='brand-container'>
        <router-link class='link-brand' to="/">
          <img :src='icn_brand' alt=""/>
          GG
        </router-link>
      </div>

      <div class='right-nav'>
        <ul class='gg-ul'>
          <router-link class='link' to="/"><li class='gg-li'>Home</li></router-link>
          <router-link class='link' to="/games"><li class='gg-li'>Games</li></router-link>
          <router-link class='link' to="/news"><li class='gg-li'>News</li></router-link>
          <router-link class='link' to="/careers"><li class='gg-li'>Careers</li></router-link>
          <router-link class='link' to="/contact"><li class='gg-li'>Contact</li></router-link>
          <router-link class='link' to="/about"><li class='gg-li'>About</li></router-link>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data: _ => {
    return {
      icn_brand: require('@/assets/textures/brand-icon.png')
    }
  }
}
</script>

<style scoped lang='scss'>
@import '@/styles/global.scss';
@import '@/styles/list.scss';

$margin-width: 70px;

.header-container {
  background-image: linear-gradient($BGColor1, rgb(10, 10, 10));
  font-weight: 600;
  &::after{
    content: '';
    display: table;
    clear: both;
  }
}

.nav-container {
  color: white;
  margin: 0 $margin-width;
}

.brand-container {
  float: none;
  text-align: center;
  a { justify-content: center; }

  @media screen and (min-width: $device-sm) {
    float: left;
    text-align: unset;
    a { justify-content: unset; }
  }
}

.right-nav {
  float: none;
  text-align: center;
  ul { display: block; }

  @media screen and (min-width: $device-sm) {
    float: right;
    text-align: unset;
    ul {  display: flex; padding: 0; margin: 0;}
  }
}

.link-brand {
  display: flex;
  line-height: 50px;
  text-decoration: none;
  color: white;
}

.link {
  text-decoration: none;
  color: white;

  a {
    text-decoration:none;
    color: white;
  }

  &:hover {
    transition: 0.3s;
    background-color: rgb(77, 77, 77);
  }
}
</style>
