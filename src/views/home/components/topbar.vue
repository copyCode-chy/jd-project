<template>
  <div class="top-img" style="background-color: rgb(4, 26, 118);">
    <a href="#">
      <div class="bgi">
        <i class="iconfont icon-guanbi close"></i>
      </div>
    </a>
  </div>

  <div class="topbar">
    <div class=" topbar-container">
      <div class="leftbar">
        <ul>
          <li v-for="item in leftArr" :key="item.name">
            <a href="#">
              {{ item.name }}
              <i class="iconfont icon-35_xiangxiajiantou" v-if="item.icon"></i>
            </a>
          </li>
        </ul>
      </div>
      <div class="rightbar">
        <ul>
          <li v-for="item in rightArr" :key="item.name">
            <a href="#">
              <i v-if="item.type" class="iconfont icon-gouwuche cart"></i>
              {{ item.name }}
              <i class="iconfont icon-35_xiangxiajiantou" v-if="item.icon"></i>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </div>

</template>

<script setup>
const leftArr = [
  { name: '中国大陆版 - 广西', icon: true },
  { name: '你好, 请登录' },
  { name: '免费注册' },
  { name: '切换至企业版' },
]

const rightArr = [
  { name: '购物车', type: 'cart' },
  { name: '我的订单' },
  { name: '我的京东', icon: true },
  { name: '企业采购', icon: true },
  { name: '商务服务', icon: true },
  { name: '网站导航', icon: true },
  { name: '手机京东', icon: true },
  { name: '网站无障碍' },
]
</script>

<style lang="scss" scoped>
.top-img {
  width: 100% !important;
  height: 60px;

  a {
    display: block;
    width: 1292.8px;
    height: 100%;
    margin: auto;

    .bgi {
      position: relative;
      background-image: url(../../../assets/images/topbar.jpg);
      background-repeat: no-repeat;
      background-size: auto 100%;
      background-position: center;
      height: 100%;

      .close {
        position: absolute;
        right: 0;
        top: 0;
        width: 20px;
        height: 20px;
        background-color: rgba(45, 44, 44, 0.5);
        color: rgb(183, 181, 181);
        font-weight: 600;
        /* 居中字体图标 */
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 5px;
      }
    }
  }
}

.topbar {
  border-bottom: 1px solid rgb(80, 82, 89, 0.1);

  .topbar-container {
    width: 1292.8px;
    margin: auto;
    height: 36px;
    font-size: 12px;
    display: flex;
    justify-content: space-between;
    line-height: 36px;

    .leftbar {
      ul {
        display: flex;
        justify-content: left;
      }
    }

    .rightbar {
      ul {
        display: flex;
        justify-content: right;

        .cart {
          font-size: 14px;
          color: rgb(247, 52, 69);
        }
      }
    }

    a {
      color: rgb(80, 82, 89);

      &:hover {
        color: rgb(255, 15, 35);
      }
    }

    .spacer {
      width: 0.5px;
      height: 8px;
      display: inline-block;
      background-color: rgba(0, 0, 0, 0.2);
      margin: 0 8px;
    }

    .iconfont {
      font-size: 10px;
      margin: 2px 0 0 2px;
    }

    li:not(:last-child)::after {
      content: '';
      width: 0.5px;
      height: 8px;
      display: inline-block;
      background-color: rgba(0, 0, 0, 0.2);
      margin: 0 8px;
    }
  }
}
</style>