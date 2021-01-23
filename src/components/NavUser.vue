<template>
<div class="navheader-box">
  <div class="navheader">
    <div class="pages">
      <ul>
        <li>logo</li>
        <li>主站</li>
        <li>番剧</li>
        <li>漫画</li>
        <li>下载App</li>
      </ul>
    </div>
    <div class="search">
      <form action="">
        <input type="text">
        <div class="nav_search_btn">
          <button type="button" class="nav-search-submit"></button>
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
.navheader-box {
  min-width: 650px;
  height: 56px;
  position:absolute;
  width: 100%;
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
        .nav_search_btn {
          position: absolute;
          right: 0;
          top: 0;
          margin: 0;
          padding: 0;
          width: 48px;
          height: 36px;
          border: none;
          border-radius: 2px;
          background: #e7e7e7;
          cursor: pointer;
          .nav-search-submit::before{
            content:"\E72C";
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
