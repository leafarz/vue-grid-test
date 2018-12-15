<template>
  <div>
    <header>
      <Header />
    </header>
    <body>
      <router-view/>
    </body>

    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'

export default {
  name: 'app',
  components: {
    Header,
    Footer
  }
}
</script>

<style>
@font-face {
  font-family: 'Titillium Web';
  font-style: normal;
  font-weight: 400;
  src: url('./assets/fonts/Tillium\ Web/TitilliumWeb-Regular.ttf') format('truetype');
}

@font-face {
  font-family: 'Titillium Web';
  font-style: normal;
  font-weight: 700;
  src: url('./assets/fonts/Tillium\ Web/TitilliumWeb-Bold.ttf') format('truetype');
}

@font-face {
  font-family: 'Titillium Web';
  font-style: normal;
  font-weight: 600;
  src: url('./assets/fonts/Tillium\ Web/TitilliumWeb-Bold.ttf') format('truetype');
}

* {
  padding: 0;
  margin: 0;
  font-family: 'Titillium Web';
}
</style>
