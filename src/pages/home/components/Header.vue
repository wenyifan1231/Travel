<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';

.header {
  display: flex;
  line-height: 0.86rem; /* 43/50 */
  background: $bgcolor;
  color: #fff;

  .header-left {
    width: 0.64rem; /* 32/50 */
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.4rem; /* 20/50 */
    }
  }

  .header-input {
    flex: 1;
    height: 0.64rem; /* 32/50 */
    line-height: 0.64rem; /* 32/50 */
    margin-top: 0.12rem; /* 6/50 */
    margin-left: 0.2rem; /* 10/50 */
    padding-left: 0.2rem; /* 10/50 */
    background-color: #fff;
    color: #ccc;
    border-radius: 0.1rem; /* 5/50 */
  }

  .header-right {
    width: 1.24rem; /* 62/50 */
    float: right;
    text-align: center;

    .arrow-icon {
      font-size: 0.24rem; /* 12/50 */
    }
  }
}
</style>
