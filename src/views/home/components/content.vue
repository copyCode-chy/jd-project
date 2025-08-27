<template>
  <div class="content">
    <div class="left-content">
      <ul>
        <li v-for="item in contentList" :key="item.id">
          <i class="iconfont icon-gouwuche"></i>
          <span v-for="(sub, index) in item.value" :key="sub">
            <a href="#">{{ sub }}</a>
            <span v-if="index < item.value.length - 1"> / </span>
          </span>
        </li>
      </ul>
    </div>
    <div class="middle-content">2</div>
    <div class="right-content">3</div>
  </div>
</template>

<script setup>

const contentList = [
  { value: ['家用电器'], id: '111' },
  { value: ['手机', '运营商', '数码'], id: '112' },
  { value: ['电脑', '办公', '文具用品'], id: '113' },
  { value: ['家居', '家具', '家装', '厨具'], id: '114' },
  { value: ['男装', '女装', '童装', '内衣'], id: '115' },
  { value: ['美妆', '个护', '清洁'], id: '116' },
  { value: ['母婴', '玩具乐器'], id: '117' },
  { value: ['食品', '酒类', '生鲜'], id: '118' },
  { value: ['男鞋', '运动', '户外'], id: '119' },
  { value: ['汽车', '用品'], id: '120' },
  { value: ['房产', '汽车', '汽车用品'], id: '121' },
]
</script>

<style lang="scss" scoped>
.content {
  padding: 16px;
  display: flex;
  justify-content: space-between;
  background-color: white;
  border-radius: 12px;

  .left-content {
    width: 248px;
    background-color: #F7F8FC;
    border-radius: 8px;

    ul {
      padding: 8px 0;

      li {
        padding-left: 18px;
        height: 34px;
        line-height: 34px;

        &:hover {
          background-color: #d9d9d9;
        }

        i {
          margin-right: 8px;
        }

        a {
          font-family: PingFang SC;
          font-size: 14px;
          color: #1A1A1A;

          &:hover {
            color: #ff0f23;
            border-bottom: #ff0f23 1px solid;
          }
        }
      }
    }
  }
}
</style>