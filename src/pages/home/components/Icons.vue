<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page,index) in pages" :key="index">
        <div class="icon" v-for="item in page" :key="item.id">
          <div class="icon-img">
            <img
              class="icon-img-content"
              :src="item.imgUrl"
            >
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOption: {},
      iconList: [{
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      },
      {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
        desc: '一日游'
      },
      {
        id: '03',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
        desc: '动植物园'
      },
      {
        id: '04',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png',
        desc: '踏青赏花'
      },
      {
        id: '05',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/47/c2b659e048b11602.png',
        desc: '遛娃儿'
      },
      {
        id: '06',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/437aad2dd0c1edb38fee0c51f8f9dd02.png',
        desc: '精彩演出'
      },
      {
        id: '07',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/de711920c71e38287d9f95f7910aa1aa.png',
        desc: '精品小团'
      },
      {
        id: '08',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/fa/2548667cb6e902.png',
        desc: '展馆展览'
      },
      {
        id: '09',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
        desc: '游船观光'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.icons >>> .swiper-container {
  height: 0;
  overflow: hidden;
  padding-bottom: 50%;

  .icon {
    overflow: hidden;
    width: 25%;
    float: left;
    height: 0;
    padding-bottom: 25%;
    position: relative;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem; /* 22/50 */
      box-sizing: borderbox;
      padding: 0.1rem; /* 5/50 */

      .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem; /* 22/50 */
      line-height: 0.44rem; /* 22/50 */
      color: $textColor;
      text-align: center;
      font-size: 0.28rem; /* 14/50 */
      overflow: hidden
      white-space:nowrap
      text-overflow:ellipsis
    }
  }
}
</style>
