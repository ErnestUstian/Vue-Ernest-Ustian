<script setup>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'

let eyeImage = ref('')
let bodyImage = ref('')
let legImage = ref('')
let shoeImage = ref('')

const eyes = [
  {
    name: 'Eyes1',
    img: 'https://clipartix.com/wp-content/uploads/2018/03/big-cartoon-eyes-clipart-2018-19.png'
  },
  {
    name: 'Eyes2',
    img: 'https://cdn.pixabay.com/photo/2021/11/10/07/41/eyes-6783236_1280.png'
  },
  {
    name: 'Eyes3',
    img: 'https://creazilla-store.fra1.digitaloceanspaces.com/cliparts/75170/funny-cartoon-eyes-clipart-xl.png'
  },
  {
    name: 'Eyes4',
    img: 'https://cdn1.iconfinder.com/data/icons/travel-104/64/Travel_Vacation_Tourism-11-512.png'
  }
]
const bodies = [
  {
    name: 'Body1',
    img: 'https://www.harvardpubliclibrary.org/sites/default/files/tshirt.png'
  },
  {
    name: 'Body2',
    img: 'https://cdn0.iconfinder.com/data/icons/clothes-icons-set-cartoon-style/512/a699-512.png'
  },
  {
    name: 'Body3',
    img: 'https://cdn.shopify.com/s/files/1/0015/2602/products/CartoonMain.png?v=1651774819.png'
  },
  {
    name: 'Body4',
    img: 'https://cdn.shopify.com/s/files/1/0222/7924/products/t-shirts-cartoon-seven-t-shirt-royal-s-12116659372092.png?v=1604613776.png'
  }
]
const legs = [
  {
    name: 'Legs1',
    img: 'https://cdn2.iconfinder.com/data/icons/winter-clothes-cartoon/512/a1755-512.png'
  },
  {
    name: 'Legs2',
    img: 'https://img.freepik.com/free-icon/trousers_318-356852.jpg?w=2000'
  },
  {
    name: 'Legs3',
    img: 'https://cdn2.iconfinder.com/data/icons/snowboarding-cartoon/512/a1814-512.png'
  },
  {
    name: 'Legs4',
    img: 'https://img.freepik.com/free-icon/trousers_318-766417.jpg'
  }
]
const shoes = [
  {
    name: 'Shoes1',
    img: 'https://d29fhpw069ctt2.cloudfront.net/clipart/106299/preview/Monster_Shoes_by_Merlin2525_preview_4766.png'
  },
  {
    name: 'Shoes2',
    img: 'https://creazilla-store.fra1.digitaloceanspaces.com/cliparts/7826420/sneakers-shoes-clipart-md.png'
  },
  {
    name: 'Shoes3',
    img: 'https://freepngimg.com/thumb/shoes/24652-8-shoes-clipart.png'
  },
  {
    name: 'Shoes4',
    img: 'http://www.clker.com/cliparts/l/b/A/t/e/t/forest-green-tennis-shoes-hi.png'
  }
]


const StickMan = {
  name: 'StickMan',
  img: 'https://upload.wikimedia.org/wikipedia/commons/3/35/Basic_human_drawing.png'
}

</script>
<template>

<div class="BodyParts">
    <button v-for="eye in eyes" @click="eyeImage = eye.img">
      <img :src="eye.img" draggable="false"/>
    </button>
    <button v-for="body in bodies"  @click="bodyImage = body.img">
      <img :src="body.img" draggable="false" />
    </button>
    <button v-for="leg in legs"  @click="legImage = leg.img">
      <img :src="leg.img" draggable="false"/>
    </button>
    <button v-for="shoe in shoes" @click="shoeImage = shoe.img">
      <img :src="shoe.img" draggable="false"/>
    </button>
  </div>

  <div class="StickManPlaces">
    <img id="stickman" :src="StickMan.img" class="StickManPosition" />
    <img :src="eyeImage" alt="Basic Eyes" class="EyePosition" />
    <img :src="bodyImage" alt="" class="BodyPosition" />
    <img :src="legImage" alt="" class="LegPosition" />
    <img :src="shoeImage" alt="" class="ShoePosition" />
  </div>



</template>

<style scoped>
html,
body,
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-size: 62.5%;
}

.BodyParts {
  display: flex;
  flex-direction: column;
}

.StickManPlaces {
  position: relative;
}
#stickman {
  display: absolute;
  width: 150%;
  height: 150%;
}
.EyePosition {
  position: absolute;
  right: 0%;
  width: 50%;
  height: auto;
  top: 15%;
}
.BodyPosition {
  position: absolute;
  left: 27.253245%;
  width: 100%;
  height: 50%;
  top: 45%;
}
.LegPosition {
  position: absolute;
  left: 27.253245%;
  width: 100%;
  height: auto;
  top: 87.5%;
}
.ShoePosition {
  position: absolute;
  left: -35%;
  width: 200%;
  height: auto;
  top: 120%;
}

img {
  width: 100px;
  height: 100px;
}
</style>
