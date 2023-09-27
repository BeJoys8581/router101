<script setup>
import { ref } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const id = parseInt(route.params.id);

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
 <!-- Tea Products -->
 <div class="bg-body-tertiary me-md-3 pt-3 px-3 pt-md-5 px-md-5 text-center overflow-hidden">
    <div class="my-3 p-3">
    <RouterLink to="/" class="btn-back">Back</RouterLink>
    <h2 class="display-5">{{ TeaList[id - 1].name }}</h2>
      <p class="lead">Joys in Every Sip {{ id }}</p>
    </div>
    <div class="mx-auto" style="width: 45%; height: 320px; margin-top: -20px; border-radius: 21px 21px 0 0;">
      <img :src="TeaList[id - 1].img" width="500" height="350" style="margin-top: 1px;" />
    </div> <br> <br>
    The ambiance is warm, inviting, and infused with a touch of vintage charm. Soft instrumental music plays in the background, 
    creating a soothing atmosphere for patrons. The interior is decorated with a mix of wooden furniture, comfortable cushions,
     and soft lighting, giving the space a cozy and intimate feel.
 <br> <br> <br> </div> 
  </template>
  


<style>
.btn-back {
 display: flex;
 height: 3em;
 width: 100px;
 align-items: center;
 justify-content: center;
 background-color: #eeeeee4b;
 border-radius: 3px;
 letter-spacing: 1px;
 transition: all 0.2s linear;
 cursor: pointer;
 border: none;
 background: #fff;
}

.btn-back > svg {
 margin-right: 5px;
 margin-left: 5px;
 font-size: 20px;
 transition: all 0.4s ease-in;
}

.btn-back:hover > svg {
 font-size: 1.2em;
 transform: translateX(-5px);
}

.btn-back:hover {
 box-shadow: 9px 9px 33px #d1d1d1, -9px -9px 33px #ffffff;
 transform: translateY(-2px);
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