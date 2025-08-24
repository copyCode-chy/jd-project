<template>
  <div class="aside-menu">
    <ul>
      <li v-for="item in menuItems" :key="item.id">
        <a href="#">
          <i class="iconfont" :class="item.icon"></i>
          <span>{{ item.name }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script setup>
const menuItems = [
  { name: '购物车', id: 1, icon: 'icon-gouwuche' },
  { name: '我的', id: 2, icon: 'icon-wode' },
  { name: '客服', id: 3, icon: 'icon-kefu' },
  { name: '反馈', id: 4, icon: 'icon-yijianfankui' },
  { name: '回顶部', id: 5, icon: 'icon-dingbu' },
];
</script>

<style lang="scss" scoped>
.aside-menu {
  border-radius: 10px 0 0 10px;
  font-size: 12px;
  background-color: white;

  ul {
    width: 44px;
    border-radius: 10px 0 0 10px;
    padding: 0;
    margin: 0;
    list-style: none;
    overflow: hidden;

    li {
      width: 44px;
      height: 70px;
      display: flex;
      align-items: center;
      justify-content: center;

      a {
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        text-decoration: none;
        color: #333;

        &:hover {
          background-color: rgb(255, 15, 35);
          color: white !important;
          transition: all 0.3s;

          span {
            color: white !important;
          }
        }

        i {
          font-size: 20px;
          line-height: 1;
          display: block;
          margin-bottom: 4px;
        }

        span {
          font-size: 12px;
        }
      }

      &:last-child a span {
        color: rgb(225, 37, 27);
      }
    }
  }
}
</style>
