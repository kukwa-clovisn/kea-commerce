<template>
  <div class="main">

<el-carousel :interval="5000" arrow="always" direction="horizontal">
 <el-carousel-item v-for="(image,index) in images" :key="index" >

  <div class="blur-wrapper"></div>

   <img :src="image" />

 </el-carousel-item>
</el-carousel>

</div>
</template>

<script>
import {ref} from 'vue';
export default{
  name:'slider',
  props:{
       images: {type:Array}
  },
  setup(props){
       const images = ref(props.images) ;
       return{ 
       images
  }
  }

}
</script>

<style lang="scss" scoped>
.main{ 
 width:100%;
 height:100%;
 overflow-x:hidden;
 margin:0 auto;
}

img{ 
 height:100%;
 width:100%;
 object-fit: cover;
}


.el-carousel.el-carousel--horizontal{ 
width:100% !important;
height:100%;
margin:0;
padding:0;

.el-carousel__container{ 
 
    .el-carousel__item{ 
  
         height:100% !important;
       }
    }
}

</style>