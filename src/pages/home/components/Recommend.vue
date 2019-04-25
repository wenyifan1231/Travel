<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendLIst" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendLIst: [
        {
          id: '01',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1904/65/65a949083122447da3.img.jpg_200x200_c4b2f699.jpg',
          title: '上海迪士尼乐园',
          desc: '全球最大的迪士尼城堡'
        },
        {
          id: '02',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1904/d5/d579b03a110d75a8a3.img.jpg_200x200_740bd4c0.jpg',
          title: '上海野生动物园',
          desc: '会跳芭蕾的小海狮们~'
        },
        {
          id: '03',
          imgUrl:
            'http://img1.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_200x200_9a7794fc.jpg',
          title: '上海欢乐谷',
          desc: '敢上1200米长的木质过山车吗？'
        },
        {
          id: '04',
          imgUrl:
            'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
          title: '上海东方明珠',
          desc: '259米透明悬空观光廊了解一下~'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.recommend-title {
  margin-top: 0.2rem; /* 10/50 */
  line-height: 0.8rem; /* 40/50 */
  background: #eee;
  text-indent: 0.2rem; /* 10/50 */
}

.item {
  overflow: hidden;
  display: flex;
  height: 1.88rem; /* 94/50 */

  .item-img {
    width: 1.7rem; /* 85/50 */
    height: 1.7rem; /* 85/50 */
    padding: 0.1rem; /* 5/50 */
  }

  .item-info {
    flex: 1;
    padding: 0.1rem; /* 5/50 */
    min-width: 0;

    .item-title {
      line-height: 0.54rem; /* 27/50 */
      font-size: 0.32rem; /* 16/50 */
      ellipsis();
    }

    .item-desc {
      line-height: 0.4rem; /* 20/50 */
      color: #aaa;
      ellipsis();
    }

    .item-btn {
      background: #ff9300;
      color: #fff;
      padding: 0 0.2rem; /* 10/50 */
      border-radius: 0.06rem; /* 3/50 */
      margin-top: 0.2rem; /* 10/50 */
      line-height: 0.44rem; /* 22/50 */
    }
  }
}
</style>
