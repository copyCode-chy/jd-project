<template>
  <div class="header-bar">
    <div class="header-left-logo">
      <a href="#">
        <img src="../../../assets/images/logo.png" alt="">
      </a>
    </div>

    <div class="header-searchBox">
      <div class="search-top">
        <div class="input-text">
          <div class="select">
            <a href="#">
              <span class="select-text">商品</span>
              <img src="../../../assets/images/icon.png" alt="">
            </a>
          </div>
          <input type="text" placeholder="搜索 商品/品牌/品类">
          <span class="search-icon">
            <a href="#">
              <i class="iconfont icon-05"></i>
            </a>
          </span>
          <button>搜索</button>
        </div>

        <div class="right-ai">
          <a href="#">
            <img src="../../../assets/images/ai.png" alt="">
            <span>京言AI</span>
          </a>
        </div>
      </div>

      <div class="search-keywords">
        <ul>
          <li v-for="item in searchKeywords" :key="item.id">
            <a href="#">{{ item.name }}</a>
          </li>
        </ul>
      </div>
    </div>

    <div class="header-right-ads">
      <a href="#"></a>
    </div>
  </div>
</template>

<script setup>
const searchKeywords = [
  {
    name: '开学季必买好物',
    id: '111'
  },
  {
    name: '零食广场五折起',
    id: '222'
  },
  {
    name: '黛珂小紫瓶',
    id: '333'
  },
  {
    name: 'wakuku一代',
    id: '444'
  },
  {
    name: '浪浪山小妖怪',
    id: '555'
  },
  {
    name: '烘焙粉',
    id: '666'
  },
  {
    name: 'IKEA宜家家居',
    id: '777'
  }
]
</script>

<style lang="scss" scoped>
.header-bar {
  height: 134px;
  display: flex;
  justify-content: space-between;
  align-items: center;

  .header-left-logo {
    width: 240px;
    height: 70px;

    a {
      display: block;
      width: 100%;
      height: 100%;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }

  .header-searchBox {
    .search-top {
      display: flex;

      .input-text {
        width: 687px;
        height: 44px;
        border: 2px solid rgb(255, 15, 35);
        border-radius: 8px;
        display: flex; // 让整个搜索框走 flex
        align-items: center;
        line-height: normal;
        font-size: 14px;
        vertical-align: middle;
        text-align: center;
        position: relative;

        .select {
          position: absolute;
          left: 20px;
          width: 77px;
          height: 100%;

          a {
            display: flex;
            align-items: center;
            color: #1A1A1A;
            font-size: 14px;
            font-weight: 500;
            height: 100%;
            line-height: normal;

            .select-text {
              vertical-align: middle;
            }

            img {
              width: 8px;
              height: 8px;
              margin-left: 4px;
              vertical-align: middle;
            }
          }
        }

        input {
          width: 462px;
          height: 36px;
          padding: 2px 128px 2px 90px;
          border: none;
          border-radius: 8px;
          outline: none; // 把默认焦点高亮去掉
          line-height: 32px;
        }

        button {
          border-radius: 6px;
          position: absolute;
          right: 2px;
          top: 50%;
          transform: translateY(-50%);
          width: 80px;
          height: 36px;
          border: none;
          background-color: #FF0F23;
          font-size: 16px;
          font-weight: 600;
          color: #fff;
          cursor: pointer;
        }

        .search-icon {
          position: absolute;
          right: 100px;

          a {
            i {
              font-size: 20px;
              color: #666;
            }
          }
        }
      }

      .right-ai {
        width: 102px;
        height: 44px;
        margin-left: 20px;
        border-radius: 8px;
        background: #FFFFFF;
        border: 1px solid #ff477f;
        display: flex;
        align-items: center;
        justify-content: center;

        a {
          color: #FF477F;
          font-family: PingFang SC;
          font-size: 16px;
          font-weight: 700;
          line-height: 44px;

          img {
            width: 20px;
            height: 16px;
            vertical-align: middle;
            margin-right: 6px;
          }

          span {
            vertical-align: middle;
          }
        }
      }
    }

    .search-keywords {
      margin-top: 10px;

      ul {
        display: flex;

        li {
          margin-right: 12px;

          a {
            font-size: 14px;
            font-family: PingFang SC;
            color: #505259;
            text-decoration: none;
          }

          &:nth-child(-n+2) {
            a {
              color: #FF0F23;
            }
          }

          &:nth-child(n+3) {
            a:hover {
              color: #c81623;
            }
          }
        }
      }
    }
  }

  .header-right-ads {
    width: 160px;
    height: 70px;

    a {
      display: block;
      width: 100%;
      height: 100%;
      background-image: url('//m.360buyimg.com/babel/jfs/t1/306335/9/4387/173406/004f0601F093ecfc9/aed6fb3f8a6871b2.gif');
      background-repeat: no-repeat;
      background-size: 160px 70px;
    }
  }
}
</style>