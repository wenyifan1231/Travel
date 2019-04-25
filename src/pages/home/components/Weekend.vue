<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendLIst" :key="item.id">
        <div class="item-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendLIst: [
        {
          id: '01',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
          title: '上海必打卡',
          desc: '中西合璧，现代和传统各有各的精彩'
        },
        {
          id: '02',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1603/cf/762cb38938a093.jpg_r_640x214_e02c18ef.jpg',
          title: '上海看花',
          desc: '这个好天气，一起去看花吧~'
        },
        {
          id: '03',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg',
          title: '周末亲子爱玩',
          desc:
            '走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~'
        },
        {
          id: '04',
          imgUrl:
            'http://img1.qunarzz.com/sight/source/1511/1d/fe098e8cfec117.jpg_r_640x214_a9be292a.jpg',
          title: '上海城市观光',
          desc:
            '来这里寻找你所不认识的魔都 ，感受云端漫步，品味老上海风情，享受休闲时光'
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

.item-wrapper {
  overflow: hidden;
  height: 0;
  padding-bottom: 37.8%;

  .item-img {
    width: 100%;
  }
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
}
</style>
