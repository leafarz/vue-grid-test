<template>
  <div class='container'>
    <div class='grid-container'>
      <div class='grid-item'>
        <h1>Navigation</h1>
        <ul>
          <li><a href='/'>Home</a></li>
          <li><a href='/games'>Games</a></li>
          <li><a href='/news'>News</a></li>
        </ul>
      </div>

      <div class='grid-item'>
        <ul>
          <h1>Social</h1>
          <li><a href='#facebook'><img :src='icn_fb' alt=""/> Facebook</a></li>
          <li><a href='#twitter'><img :src='icn_twitter' alt=""/> Twitter</a></li>
          <li><a href='#instagram'><img :src='icn_ig' alt=""/> Instagram</a></li>
        </ul>
      </div>

      <div class='grid-item'>
        <ul>
          <h1>Information</h1>
          <li><a href='#terms-conditions'>Terms & Conditions</a></li>
          <li><a href='#private-policy'>Private Policy</a></li>
          <li><a href='#careers'>Careers</a></li>
          <li><a href='#contact-us'>Contact Us</a></li>
          <li><a href='#about'>About</a></li>
          </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: _ => {
    return {
      icn_fb: require('@/assets/textures/webicon-facebook-s.png'),
      icn_twitter: require('@/assets/textures/webicon-twitter-s.png'),
      icn_ig: require('@/assets/textures/webicon-instagram-s.png')
    }
  }
}
</script>

<style scoped lang='scss'>
@import '@/styles/global.scss';

ul {
  list-style-type: none;
  text-decoration: none;
}

li {
  padding: 5px 0;
  a {
    text-decoration: none;
    color: white;

    &:hover {
      text-decoration: underline;
    }
  }
}

.container {
  background-color: $BGColor2;
  color: white;
  text-align: center;
}

.grid-container {
  display: block;
  padding: 0;
  grid-gap: 0;

  @media screen and (min-width: $device-sm) {
    display: grid;
    grid-template-columns: repeat( 3, 1fr);
    padding: 20px;
    grid-gap: 20px;
  }
}

.grid-item {
  padding: 20px;
  text-align: left;
  h1 { padding: 0; }

  @media screen and (max-width: $device-sm) {
    &:nth-child(even) {
      background-color: rgba(30, 30, 30, 0.9);
    }
  }

  @media screen and (min-width: $device-sm) {
    text-align: center;
    h1 { padding: 20px; }
  }
}
</style>
