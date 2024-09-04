<script setup>

   import {defineProps} from "vue";


   const props = defineProps (["name" , "description" ,"image" , "onDelete" , "id" ]);

   const handleDelete = () => {
  props.onDelete(props.id); // Вызываем функцию удаления с id поста
};


   
</script>

<template>
     <li>
          <img :src=props.image alt="изображение">
          <h3 class="post__title">{{ props.name}}</h3>
          <p class="description__title">{{  props.description }}</p>
          <button @click="handleDelete">Удалить</button> <!-- Кнопка удаления -->
        </li>
</template>

<style scoped>

img {
  width: 500px; 
  height: 500px; 
  border-top-right-radius: 20px;
  border-top-left-radius: 20px;
}

li {
   background-color: rgb(240, 239, 239);
   font-family: "log";
   height: 700px;
   width: 500px;
   box-shadow: 1px;
   text-align: center;
   border-radius: 20px;
}

.post__title {
   font-family: "log";
   font-size: 25px;
   margin-bottom: 10px;
}

.description__title {
   font-family: "log";
   font-size: 15px;

}

@media (max-width:1070px) {
   li {
   height: 500px;
   width: 300px;
}

img {
  width: 300px; 
  height: 300px; 
  border-top-right-radius: 20px;
  border-top-left-radius: 20px;
}

   
}

</style>