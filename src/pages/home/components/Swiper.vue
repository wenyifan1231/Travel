<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>

      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 2000
      },
      swiperList: [
        {
          id: '01',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e0c5d91cb9b435518bb223b81b70874e.jpg_750x200_f2d5c66a.jpg'
        },
        {
          id: '02',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/e9f92741ef8b1cb0472ced96150d0d1c.jpg_750x200_1f0a2392.jpg'
        },
        {
          id: '03',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/33941bbe8d3921f7b7089f07187b5442.jpg_750x200_947ed0f6.jpg'
        },
        {
          id: '04',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/a9658b2ee2c2c6de227c9710a8b04d48.jpg_750x200_f38fba28.jpg'
        },
        {
          id: '05',
          imgUrl:
            'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/d7bbc21db442366a882e04ddc984669a.jpg_750x200_85e640d9.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
  background-color: #fff;
}

.wrapper {
  width: 100%;
  height: 0;
  overflow: hidden;
  padding-bottom: 26.667%;
  background-color: #eee;
}

.swiper-img {
  width: 100%;
}
</style>
