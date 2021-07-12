<template>
  <body>

  <div class="header-wrapper">
    <header>
      <div class="container">
        <div class="logo-container">
          <!-- Website Logo -->
          <p id="bigname"><strong>Knowledge Base Theme</strong></p>
          <span class="tag-line">Premium WordPress Theme</span>
        </div>

        <!-- Start of Main Navigation -->
        <nav class="main-nav">
          <div class="menu-top-menu-container">
            <ul id="menu-top-menu" class="clearfix">
              <li class="current-menu-item"><a href="/menu">主页</a></li>
              <li><a href="/allArticle">所有文章</a></li>
              <li><a href="/myArticle">我的文章</a></li>
              <li><a href="/myComment">我的评论</a></li>
              <li><a href="/personalKeep">个人中心</a></li>
            </ul>
          </div>
        </nav>
        <!-- End of Main Navigation -->

      </div>
    </header>
  </div>

  <div id="page-wraper">
    <!-- Sidebar Menu -->
    <div class="responsive-nav">
      <i class="fa fa-bars" id="menu-toggle"></i>
      <div id="menu" class="menu">
        <i class="fa fa-times" id="menu-close"></i>
        <div class="container">
          <div class="image">
            <a href="#"><img src="../../assets/wallpaper.jpg" alt="" /></a>
          </div>
          <div class="author-content">
            <h4>Name</h4>
            <span>个性签名</span>
          </div>
          <nav class="main-nav2" role="navigation">
            <ul class="main-menu">
              <li><a href="/personalKeep">个人信息</a></li>
              <li><a href="personalPage">个人主页</a></li>
              <li><a href="/changePassword">修改密码</a></li>
              <li><a href="/changeHead">修改头像及背景</a></li>
              <li><a href="/voice">语音设置</a></li>
              <li><a href="/edit">写文章</a></li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
  </div>

  <h3>修改头像</h3>
  <form action="#">
    <label>图片预览</label>
    <div class="headimage">
      <a  href="#"><img src="../../assets/wallpaper.jpg" alt="" /></a>
    </div>
    <label>上传图片</label>
    <input name="demail" value="" type="file" size="30" accept="image/gif image/jpeg,image/png,image/jpg "  />
    <br>
    <br>
    <button id="keep" @click="keeper">上传</button>
  </form>

  <h3>修改主页背景</h3>
  <form action="#">
    <label>图片预览</label>
    <div class="headimage">
      <a  href="#"><img src="../../assets/wallpaper.jpg" alt="" /></a>
    </div>
    <label>上传图片</label>
    <input name="demail" value="" type="file" size="30" accept="image/gif image/jpeg,image/png,image/jpg "  />
    <br>
    <br>
    <butoon id="keep" @click="keeper">上传</butoon>
  </form>

  </body>
</template>

<script>
export default {
  name:
      "personal",
  methods:{
    keeper(){
      this.$router.push('/personalNot');
    }
  }
}
</script>

<style scoped>

form {
  margin:10px; padding: 0;
  border: 1px solid #f2f2f2;
  background-color: #FAFAFA;
}
label {
  display:block;
  font-weight:bold;
  margin:5px 0;
  color:black;
}
input,.form-select {
  padding: 2px;
  border:1px solid #eee;
  font: normal 1em Verdana, sans-serif;
  color:#777;
}
.text {
  width:190px;
  padding:100px;
  margin-left:auto;
  margin-right: auto;
  font: normal 1em Verdana, sans-serif;
  border:1px solid #eee;
  height:20px;
  display:block;
  color:black;
}
.headimage{
  width: 400px;
  height: 250px;
  text-align: center;
}
#keep {
  margin: 0;
  font: bold 1em Arial, Sans-serif;
  border: 1px solid #CCC;
  background: #FFF;
  padding: 2px 3px;
  color: #4284B0;
}

body {
  font-family: 'Lato', sans-serif;
}

#page-wraper {
  background: url(../../assets/wallpaper.jpg) no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  width: 100%;
}


/* Basic */

body {
  overflow-x: hidden;
}

input{
  outline: none;
}

a,
a:hover {
  text-decoration: none;
}

p {
  font-size: 16px;
  line-height: 24px;
  color: #fff;
}

h4 {
  font-size: 26px;
  font-weight: 700;
  color: #fff;
  letter-spacing: 0.25px;
}

img {
  width: 100%;
  overflow: hidden;
}

ul {
  padding: 0;
  margin: 0;
  list-style: none;
}

ul li {
  display: inline-block;
}

html {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

*,
*:before,
*:after {
  -webkit-box-sizing: inherit;
  -moz-box-sizing: inherit;
  box-sizing: inherit;
}

.container {
  margin: 0 auto;
}

.main-nav2 {
  text-align: center;
}

.main-nav2 li:last-child a {
  border-bottom: 2px solid #fff;
}

.main-nav2 li {
  display: block;
}

.main-nav2 li a {
  height: 70px;
  line-height: 70px;
  display: inline-block;
  font-size: 16px;
  font-weight: 700;
  color: #fff;
  width: 100%;
  transition: all 0.5s;
  border-top: 2px solid #fff;
}

.main-nav2 li:hover a,
.main-nav2 li.active a {
  background: #fff;
  color: #8c363e;
}

/* Sidebar Menu */

.menu .image {
  margin-top: 60px;
}

.menu .image img {
  width: 140px;
  height: 140px;
  border-radius: 50%;
  text-align: center;
}

.menu .author-content {
  margin: 40px 0px 60px 0px;
}

.menu .author-content h4 {
  margin-bottom: 0px;
}

.menu .author-content span {
  font-size: 13px;
  font-style: italic;
  color: #fff;
}

.menu {
  margin-top: 60px;
}

.menu  {
  position: relative;
  margin-top: 60px;
}
.menu:before,
.menu:after {
  content: "";
  display: table;
}

.menu:after {
  clear: both;
}

.menu a {
  text-decoration: none;
  color: inherit;
}

.menu {
  text-align: center;
}
.menu {
  left: 1%;
  -webkit-transition: -webkit-transform 233ms cubic-bezier(0, 0, 0.21, 1);
  -webkit-overflow-scrolling: touch;
  background-color: #a43f49;
  box-sizing: border-box;
  height: 100vh;
  max-height: 100vh !important;
  max-width: 80vw !important;
  min-width: 45px !important;
  outline: none;
  overflow-x: hidden !important;
  overflow-y: auto !important;
  padding: 0;
  position: fixed !important;
  top: -70px;
  width: 27%;
  will-change: transform;
  z-index: 9999 !important;
}



#menu-toggle {
  z-index: 999;
  cursor: pointer;
  position: fixed;
  top: 0;
  left: 0;
  color: #a43f49;
  background-color: #fff;
  width: 60px;
  height: 60px;
  text-align: center;
  display: inline-block;
  line-height: 60px;
}
#menu-close {
  cursor: pointer;
  text-align: right;
  color: #a43f49;
  background-color: #fff;
  width: 100%;
  height: 60px;
  text-align: center;
  display: inline-block;
  line-height: 60px;
}

.header-wrapper {
  background-color: #3b4348;
  width: 100%;
  height: auto;
}
.header-wrapper .container {
  position: relative;
  min-height: 60px;
  height: auto !important;
  height: 60px;
}
#bigname{
  color:white;
  font-size:x-large;
  margin-left: -900px;
}
.logo-container {
  padding: 19px 0;
}
.logo-container img {
  margin-right: 10px;
}
.logo-container {
  width: 450px;
}

span.tag-line {
  color: #818a90;
  font-size: 12px;
  position: relative;
  top: 2px;
}
.main-nav {
  position: absolute;
  top: 5px;
  right: 0;
}
.main-nav div > ul {
  width: auto;
  margin: 0;
}
.main-nav div > ul > li {
  position: relative;
  float: left;
  list-style: none;
  padding: 16px 14px 18px;
}
.main-nav div > ul > li a {
  font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-size: 13px;
  color: #c1cad1;
}
.main-nav div > ul > li a:hover {
  color: #fff;
}
.main-nav div > ul > li:hover > a {
  color: #fff;
}
.main-nav div > ul > li:last-child {
  padding-right: 0;
}
.main-nav div > ul li.current-menu-item a {
  color: #fff;
}
.main-nav .sub-menu {
  position: absolute;
  top: 56px;
  left: 0px;
  list-style: none;
  margin: 0;
  display: none;
}
.main-nav .sub-menu li {
  position: relative;
  background-color: #3b4348;
  padding: 6px 10px;
  width: 150px;
  cursor: pointer;
}
.main-nav .sub-menu li:hover {
  background-color: #292e32;
}
.main-nav .sub-menu li:hover > a {
  color: #fff;
}
.main-nav .sub-menu .sub-menu {
  top: 0px;
  right: 170px;
  left: auto;
}
.main-nav .responsive-nav {
  display: none;
}

/* Header - Search ---------------------------------------------------------------------------------------------------*/
.search-area-wrapper {
  background: #353b65 url("../../assets/wallpaper.jpg") center top no-repeat;
  background-size: 100%;
  min-height: 279px;
  height: 279px;
}
.search-area-wrapper .search-area {
  padding: 50px 0;
}

h3.search-header {
  font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-weight: bold;
  font-size: 36px;
  color: #fff;
  text-align: center;
}

p.search-tag-line {
  font-family: "Droid Serif", serif;
  font-style: italic;
  font-size: 18px;
  line-height: 28px;
  color: #fff;
  text-align: center;
}

form.search-form {
  margin: 40px 0 0;
  text-align: center;
}
form.search-form , form.search-form input.search-term, form.search-form input.search-btn {
  font-family: "HelveticaNeue", "Helvetica Neue", Helvetica, Arial, sans-serif;
  box-shadow: none;
  border-radius: 0;
  display: inline-block;
  border: none;
  vertical-align: bottom;
}
form.search-form input.search-term {
  font-size: 14px;
  height: 24px;
  line-height: 24px;
  padding: 12px;
  width: 72%;
  color: #858c91;
  margin-right: 10px;
  margin-bottom: 0;
}
form.search-form input.search-term.loading {
  background-image: url("../../assets/wallpaper.jpg");
  background-repeat: no-repeat;
  background-position: 98% 50%;
}
form.search-form input.search-btn {
  background-color: #3f4b55;
  font-size: 14px;
  line-height: 19px;
  font-weight: 600;
  padding: 14px 30px 15px;
  color: #fff;
}
form.search-form input.search-btn:hover {
  background-color: #4b5760;
}

#search-error-container label {
  color: #fff;
  padding: 5px;
  font-size: 14px;
}

.lt-ie8 form.search-form input.search-btn {
  padding-top: 12px;
  padding-bottom: 13px;
}

/* Page - Container --------------------------------------------------------------------------------------------------*/
.page-container {
  width: 100%;
}
.page-container > .container {
  padding: 40px 35px;
  background-color: #fff;
}


.pages-nav a {
  margin-right: 10px;
}


div {
  display: block;
  margin: 5px auto 20px auto;
}

li.comment > article {
  background: #fff;
  float: left;
  margin: 0px 10px 10px 0;
  position: relative;
  z-index: 1;
  -webkit-border-radius: 60px;
  -moz-border-radius: 60px;
  border-radius: 60px;
}
.page-content {
  margin-bottom: 20px;
}

.row.separator {
  margin-bottom: 10px;
}
.articles-list {
  margin-bottom: 20px;
}
.articles-list > h3 {
  font-weight: 600;
  margin-bottom: 20px;
  font-size: 20px;
}
.articles-list > h3 span {
  color: #6f7579;
  font-size: 16px;
}
.articles-list > h3 a {
  color: #3b4348;
}
.articles-list > h3 a:hover {
  color: #395996;
}

ul.articles {
  list-style: none;
  margin: 0;
}
ul.articles .article-entry {
  position: relative;
  border-bottom: 1px solid #f2f2f2;
  padding: 0 0 0 24px;
  background: url("../../assets/wallpaper.jpg") no-repeat 0 3px;
}
ul.articles .article-entry.standard {
  background: url("../../assets/wallpaper.jpg") no-repeat 0 3px;
}
ul.articles .article-entry.video {
  background: url("../../assets/wallpaper.jpg") no-repeat 0 3px;
}
ul.articles .article-entry.image {
  background: url("../../assets/wallpaper.jpg") no-repeat 0 3px;
}
ul.articles .article-entry {
  background: url("../../assets/wallpaper.jpg") no-repeat 0 3px;
}
ul.articles li.article-entry:last-child {
  border-bottom: 1px solid #f2f2f2;
}

.article-entry > h4 {
  font-size: 13px;
  margin-bottom: 5px;
  font-weight: 600;
}
.article-entry > h4 a {
  color: #3b4348;
}
.article-entry > h4 a:hover {
  color: #395996;
}
.article-entry .article-meta {
  display: block;
  margin-bottom: 10px;
}
.article-entry .like-count {
  position: absolute;
  bottom: 0px;
  right: 0px;
  line-height: 18px;
  font-weight: 600;
  padding: 3px 5px 3px 20px;
  border: 1px solid #f2f2f2;
  border-bottom: none;
  background: url("/liked.png") no-repeat 6px 8px;
}
.article-entry:hover .like-count {
  background: url("../../assets/wallpaper.jpg") no-repeat 6px -22px;
  color: #395996;
}

#footer .article-entry .like-count {
  border-color: #535b61;
}
#footer .article-entry:hover .like-count {
  color: #fff;
}
#footer ul.articles li.article-entry:last-child {
  border-bottom: 1px solid #535b61;
}

.main-listing article {
  margin-bottom: 0;
}
.page-container > .container {
  padding: 40px 20px;
}
@media (max-width: 767px) {
  /* Navigation */
  .main-nav > div {
    display: none;
  }

  .main-nav {
    display: block;
    width: 85%;
    margin: 10px auto;
    padding: 10px;
    border-radius: 0;
    border: none;
  }

  /* Search Area */
  .search-area-wrapper {
    background-size: auto;
    min-height: 240px;
    height: auto !important;
    height: 240px;
  }

  .search-area-wrapper .search-area {
    padding: 20px 0;
  }

  .search-area-wrapper h3.search-header {
    font-size: 30px;
    padding: 0 15px;
  }

  .search-area-wrapper p.search-tag-line {
    padding: 0 15px;
    font-size: 14px;
    line-height: 22px;
  }

  .search-area-wrapper form.search-form input.search-term {
    width: 60%;
  }

  @media (max-width: 480px) {
    /* Search Area */
    .search-area-wrapper form.search-form input.search-term {
      width: 80%;
      display: block;
      margin: 0 auto 10px;
    }

    .search-area-wrapper form.search-form input.search-btn {
      display: block;
      margin: 0 auto;
    }

    ul.articles .article-entry {
      padding-bottom: 20px;
    }
  }
  /* Menu Fix for resizing to Bigger Screen sizes */
  @media (min-width: 980px) {
    .main-nav div > ul > li {
      float: none;
      display: inline-block;
    }
  }
}
</style>