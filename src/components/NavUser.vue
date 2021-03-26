<template>
<div class="navheader-box">
  <div class="navheader">
    <div class="pages">
      <ul>
        <!-- <li></li> -->
        <li>主站</li>
        <li>番剧</li>
        <li>
          <el-popover @show="getCartoonList"
           placement="bottom-start"
           :open-delay=300
           trigger="hover">
           <div class="pop-content">
             <div class="panels" >
               <div class="panel" v-for="item in cartoonPanels" :key="item.name" >
                 <div class="img">{{item.name}}</div>
                 <div>name</div>
               </div>
             </div>
             <hr>
             <div class="list">
               <div class="list-title">人气漫画</div>
               <div v-for="(name, index) in cartoonList" :key="index">
                 <a href="javascript:;">
                   <span>{{index + 1}}</span>
                   <span>{{name.cartoonName}}</span>
                 </a>
               </div>
             </div>
           </div>
           <a href="Javascript:;" slot="reference">漫画</a>
         </el-popover>
        </li>
        <li>下载App</li>
      </ul>
    </div>
    <div class="search">
      <form action="">
        <input type="text">
        <div class="nav-search-btnbox">
          <button type="button" class="nav-search-btn icon-search">
          </button>
        </div>
      </form>
    </div>
    <div class="action">
      <ul>
        <li>user-icon</li>
        <li>大会员</li>
        <li>消息</li>
        <li>动态</li>
        <li>
          <div style="display: inline">投稿</div>
        </li>
      </ul>
    </div>
  </div>
</div>
</template>

<style lang="scss">
@import './../assets/scss/popover.scss';
.navheader-box {
  min-width: 650px;
  height: 56px;
  position:absolute;
  width: 100%;
  z-index: 1;
  .navheader {
    display: flex;
    justify-content: space-between;
    padding:10px 24px;
    line-height: 30px;
    ul {
      display: flex;
      height: 36px;
      align-items: center;
      list-style: none;
      li {
        display: inline;
        margin-right: 12px;
        min-width: 32px;
      }
    }
    .pages {
      flex:none;
    }
    .search {
      flex:1;
      max-width: 500px;
      position: relative;
      margin-right: 12px;
      form {
        padding: 0 38px 0 16px;
        border: 1px solid rgba(255, 255, 255, 0);
        border-radius: 2px;
        background-color: white;
        input {
          overflow: hidden;
          width: 100%;
          border: none;
          color: #999;
          font-size: 14px;
          outline: none;
          height: 34px;
        }
        .nav-search-btnbox {
          position: absolute;
          right: 0px;
          top: 0px;
          margin: 0;
          padding: 0;
          width: 48px;
          height: 36px;
          border: none;
          border-radius: 2px;
          background: #e7e7e7;
          .nav-search-btn {
            cursor: pointer;
            width: 100%;
            height: 100%;
            color: #505050;
            transition: all .2s;
            font-size: 14px;
          }
          .nav-search-btn:hover {
            color:#00a1d6;
          }
        }
      }
    }
    .action {
      flex:none;
    }
  }
}
</style>

<script>
export default {
  name: 'NavHeader',
  data () {
    return {
      cartoonPanels: Array,
      cartoonList: Array
    }
  },
  methods: {
    getCartoonList () {
      this.cartoonPanels = [
        { name: 1 },
        { name: 2 },
        { name: 3 },
        { name: 4 }
      ]
      this.cartoonList = [
        { cartoonName: 1 },
        { cartoonName: 2 }
      ]
    }
  }
}
</script>
