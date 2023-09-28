<script setup>
import{ ref } from "vue";

  const TeaList = ref([
    { id: 1, name: 'Tranquil Infusions', img: "https://media-cdn.tripadvisor.com/media/photo-s/28/91/1e/26/our-store.jpg" },
    { id: 2, name: 'SereniTea Corner', img: "https://cdn.shopify.com/s/files/1/0323/4735/7321/files/anotherstoryshopify_480x480.jpg?v=1582107567" },
    { id: 3, name: 'Steeped Harmony', img: "https://www.londonperfect.com/cdn-cgi/image/width=1680,height=1058,fit=cover,quality=80,format=auto,onerror=redirect,metadata=none/https://www.londonperfect.com/blog/wp-content/uploads/2018/08/TWG-Tea-Knightsbridge-3.jpg" },
    { id: 4, name: 'Mystic Brew Haven', img: "https://cdn.shopify.com/s/files/1/0323/4735/7321/files/onenimmanshopshopify_480x480.jpg?v=1582107013" },
    { id: 5, name: 'Chai Serendipity', img: "https://images.adsttc.com/media/images/5d31/fd66/284d/d1df/cf00/0142/large_jpg/Spiritea-New_Practice_Studio-7.jpg?1563557172" },
    { id: 6, name: 'Chai Chat', img: "https://static.dezeen.com/uploads/2018/10/teatulia-russell-sage-interiors-retail-bars-london-uk_dezeen_2364_col_1.jpg" }
  ]);

</script>
<template>
  <div class="container">
    <!-- Tea Products -->
    <div class="fuck">
    <div class="bg-body-tertiary pt-5 text-center "
      v-for="(Tea, index) in TeaList"
      :key="index"
    >
      <div class="my-3 p-3">
        <h2 class="display-5">{{ Tea.name }}</h2>
        <p class="lead">Joys in Every Sip {{ index+1 }}</p>
      </div>
      <div
        class="mx-auto"
        style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;"
      >
        <img :src="Tea.img" width="450" height="300" style="margin-top: 10px;" />
      </div>
      <div class="d-flex gap-2 justify-content-center ">
        <RouterLink :to="{name:'Tea', params: {id: Tea.id }}" class="button" type="button">
          Tea Details {{ index+1 }} 
        </RouterLink>
      </div>
    </div>
  </div>
  </div>
  </template>
  


<style>

img{
  width: 300px;
  height: 300px;

}

.fuck{
  display: grid;
  grid-template-columns: 1fr 1fr 1fr ;
}
.button {
 --color: #560bad;
 font-family: inherit;
 display: inline-block;
 width: 8em;
 height: 2.6em;
 line-height: 2.5em;
 margin: 20px;
 position: relative;
 overflow: hidden;
 border: 2px solid var(--color);
 transition: color .5s;
 z-index: 1;
 font-size: 17px;
 border-radius: 6px;
 font-weight: 500;
 color: var(--color);
}

.button:before {
 content: "";
 position: absolute;
 z-index: -1;
 background: var(--color);
 height: 150px;
 width: 200px;
 border-radius: 50%;
}

.button:hover {
 color: #fff;
}

.button:before {
 top: 100%;
 left: 100%;
 transition: all .7s;
}

.button:hover:before {
 top: -30px;
 left: -30px;
}

.button:active:before {
 background: #3a0ca3;
 transition: background 0s;
}

.container {
  
  max-width: 960px;
}

.icon-link > .bi {
  width: .75em;
  height: .75em;
}


.site-header {
  background-color: rgba(0, 0, 0, .85);
  -webkit-backdrop-filter: saturate(180%) blur(20px);
  backdrop-filter: saturate(180%) blur(20px);
}
.site-header a {
  color: #643400;
  transition: color .15s ease-in-out;
}
.site-header a:hover {
  color: #643400;
  text-decoration: none;
}


.product-device {
  position: absolute;
  right: 0;
  bottom: -5%;
  width: 300px;
  height: 740px;
  background-color: #003c58;
  border-radius: 21px;

}

.product-device-2 {
  left: 0;
  background-color: #003c58;
}


.flex-equal > * {
  flex: 1;
}
@media (min-width: 768px) {
  .flex-md-equal > * {
    flex: 1;
  }
}

</style>