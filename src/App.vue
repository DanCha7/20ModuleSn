<script setup>
import Footer from "/src/components/Footer.vue"
import Header from "/src/components/Header.vue";
import UnderHeader from "/src/components/UnderHeader.vue";
import Posts from "./components/Posts.vue";


</script>

<template >
     <UnderHeader />
     <Header ></Header>
     <div class="container">
          <Posts />
     </div>
     <Footer></Footer>
</template>
   
<style scoped>

.container  {
    max-width: 1600px;
    margin: auto;
    padding: 20px 20px;
}

.title__own {
    text-align: center;
    color: rgb(12, 14, 12);
    font-size: 50px;
    font-family: "log";
}

@font-face {
    font-family: "log" ;
    src: url("/src/fonts/Rubik-VariableFont_wght.ttf");
}
</style>
