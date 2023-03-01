<template>
    <div class="main">
        <el-carousel :interval="1000" type="card">
            <!-- <el-carousel-item v-for="item in 8" :key="item">
      <h3 justify="center">{{ item }}</h3>
    </el-carousel-item> -->
            <el-carousel-item v-for="(image, index) in images" :key="index">
                <div class="blur-wrapper"></div>

                <img :src="image" />

            </el-carousel-item>

        </el-carousel>

    </div>

</template>

<script>
import { ref } from 'vue'
export default {
    name: 'Carousel',
    props: {
        images: { type: Array }
    },
    setup(props) {
        const images = ref(props.images)
        return {
            images
        }
    }
}
</script>

<style lang="scss" scoped>
.main {
    width: 100%;
    height: 100%;
    overflow-x: hidden;
    margin: 0 auto;
}


button.el-carousel_arrow {
    display: flex !important;
    visibility: visible;
}

img {
    height: 100%;
    width: auto;
}


.el-carousel {
    width: 100% !important;
    height: 100%;
    margin: 0;
    padding: 0;
    position: relative;
}

.el-carousel_item {
    height: 100%;
    position: relative;
}

.el-carousel__item:nth-child(2n) {
    background-color: transparent;
}

.el-carousel__item:nth-child(2n + 1) {
    background-color: transparent;
}
</style>