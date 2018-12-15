<template>
  <div>
    <div>
      <div class='image-container'>
        <img class='headline-img' :src='img_headline' />
      </div>

      <div class='headline-text'>
        <h1>
          Lorem ipsum dolor sit, amet consectetur adipisicing elit. Dolor ullam corporis fugiat.
        </h1>
      </div>
    </div>

    <!-- ======================================== -->

    <div class='grid-main-container1'>
      <div class='grid-container-col-2'>
        <div class='grid-item1'>
          <img :src='img_pic2' alt="" />
        </div>
        <div class='grid-item1'>
          <h2>Lorem ipsum dolor, sit amet consectetur adipisicing elit.</h2>
        </div>
        <div class='grid-item1'>
          <h2>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Qui non sapiente distinctio? Est, officia accusamus!</h2>
        </div>
        <div class='grid-item1'>
          <img :src='img_pic3' alt="" />
        </div>
      </div>
    </div>

    <div class='grid-main-container2'>
      <div class='bg-image'></div>
      <div class='grid-container-col-3'>
        <div class='grid-item2'>
          <img :src='icn_sword' alt="" />
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. culpa ex ipsum deserunt tempore dolor illum, alias
               veritatis dolore ea, optio minima perferendis error voluptatum repellat explicabo cupiditate officia consequuntur.</h1>
        </div>

        <div class='grid-item2'>
          <img :src='icn_target' alt="" />
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis recusandae itaque illum laboriosam ipsam architecto!</h1>
            <h1>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Sequi vitae recusandae commodi?</h1>
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis, veritatis?</h1>
        </div>
        <div class='grid-item2'>
          <img :src='icn_shield' alt="" />
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptas sapiente, nesciunt doloremque in voluptate quisquam
             totam magni, ad dolor, architecto quibusdam cum similique?</h1>
            <h1>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis, voluptate?</h1>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data: _ => {
    return {
      img_headline: require('@/assets/textures/games01.jpeg'),
      img_pic2: require('@/assets/textures/games02.jpeg'),
      img_pic3: require('@/assets/textures/games03.jpeg'),
      icn_sword: require('@/assets/textures/sword.png'),
      icn_target: require('@/assets/textures/target.png'),
      icn_shield: require('@/assets/textures/shield.png')
    }
  }
}
</script>

<style scoped lang='scss'>
@import '@/styles/global.scss';
$img_pic4: '../assets/textures/games04.jpeg';

.image-container {
  overflow:hidden;
}
.headline-img {
  width: 100%;
  margin:-20% 0;
  filter: grayscale(50%);
}

.headline-text {
  height: 200px;
  width: 100%;
  background-image: linear-gradient(rgb(30, 30, 30), rgb(25, 25, 25), rgb(10, 10, 10));
  text-align: center;
  color: white;
  h1 {
    position: relative;
    top: 50%;
    transform: translateY(-50%);
  }
}

.bg-image {
  background-image: url($img_pic4);
  width: 100%;;
  height: 100%;;
  position: absolute;
  z-index: -1;
}

.grid-main-container1 {
  background-color: $BGColor2;
}

.grid-main-container2 {
  position: relative;
  overflow: hidden;
}

.grid-container-col-2 {
  width: 100%;
  display: block;
  padding: 0px;

  @media screen and (min-width: $device-sm) {
    display: grid;
    grid-template-columns: repeat( 2, 1fr);
    grid-gap: 20px;
    width: 80%;
    margin: auto;
  }
}

.grid-container-col-3 {
  width: 100%;
  display: block;
  padding: 0px;

  @media screen and (min-width: $device-sm) {
    display: grid;
    grid-template-columns: repeat( 3, 1fr);
    grid-gap: 50px;
    width: 80%;
    margin: auto;
  }
}

.grid-item1 {
  padding: 20px;
  color: $BodyFColor;
  h2 { text-align: center; }
  img { width: 100%; }

  @media screen and (min-width: $device-sm) {
    h2 {
      position: relative;
      top: 40%;
      transform: translateY(-50%);
    }
  }
}

.grid-item2 {
  color: $BodyFColor;
  padding: 50px;
  border-radius: 0;
  text-align: center;

  img {
    width: 100px;
  }
  h1 {
    padding: 10px;
    font-weight: 400;
  }

  @media screen and (max-width: $device-sm) {
    &:nth-child(even) {
      background-color: rgba(0, 0, 0, 0.9);
    }
    &:nth-child(odd) {
      background-color: rgba(30, 30, 30, 0.9);
    }
  }
  @media screen and (min-width: $device-sm) {
    margin: 50px 0;
    border-radius: 20px;
    background-color: rgba(0, 0, 0, 0.9);
  }
}
</style>
