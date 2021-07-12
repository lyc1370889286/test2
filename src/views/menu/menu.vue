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
  <!-- End of Header -->

  <!-- Start of Search Wrapper -->
  <div class="search-area-wrapper">
    <div class="search-area container">
      <h3 class="search-header">Have a Question?</h3>
      <p class="search-tag-line">If you have any question you can ask below or enter what you are looking for!</p>

      <form id="search-form" class="search-form clearfix" method="get" action="#" autocomplete="off">
        <input class="search-term required" type="text" id="s" name="s" placeholder="Type your search terms here" title="* Please enter a search term!" />
        <input class="search-btn" type="submit" value="Search" />
        <div id="search-error-container"></div>
      </form>
    </div>
  </div>
  <div class="page-container">
    <div class="container">
      <div class="row">

        <!-- start of page content -->
        <div class="span8 page-content">

          <!-- Basic Home Page Template -->
          <div class="row separator">
            <section class="span4 articles-list" v-for="article in articlesData" v-bind:key="article.title">
              <ul id="array-render">
                <li>
                  {{article.title}}
                </li>
              </ul>
            </section>
          </div>
        </div>
      </div>
    </div>
  </div>
  </body>
</template>

<script>

export default {
  name: "menu",

  data() {
    return {
      articlesData: {}
    }
  }
}
</script>

<style scoped>
/* General ------------------------------------------------------------------------------------------------------------*/
body {
  background-color: #fff;
}
#image1{
  width: 100px;
  height: 100px;
  border-radius: 50%;
  float:left;
  margin-left:40px;
  margin-top:15px !important;
}
.menu .image {
  margin-top: 18px;
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
  color: black;
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
  box-sizing: border-box;
  height: 54vh;
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
.information {
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
.article-entry .like-count[data-v-a70e9a84] {
  position: absolute;
  bottom: 0px;
  right: 0px;
  line-height: 18px;
  font-weight: 600;
  padding: 3px 5px 3px 20px;
  border: 1px solid #f2f2f2;
  border-bottom: none;
  background: url("../../assets/liked.png") no-repeat 6px 8px;
}
.article-entry .like-count[data-v-a70e9a84] {
  position: absolute;
  bottom: 0px;
  right: 0px;
  line-height: 18px;
  font-weight: 600;
  padding: 3px 5px 3px 20px;
  border: 1px solid #f2f2f2;
  border-bottom: none;
  background: url("#") no-repeat 6px 8px;
}
.header-wrapper {
  background-color: #3b4348;
  width: 100%;
  height: auto;
  margin-top:-61px;
}
.header-wrapper .container {
  position: relative;
  min-height: 60px;
  height: auto !important;
  top:5px;
}
#bigname{
  color:white;
  font-size:xx-large;
  margin-left: -500px !important;
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
  left:-520px;
}
.main-nav {
  position: absolute;
  top: 5px;
  left:710px;
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
  font-size: 15px;
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
  background: #353b65 url("../../assets/flower.png") center top no-repeat;
  background-size: 100%;
  min-height: 279px;
  height: auto !important;
  height: 279px;
}
.search-area-wrapper .search-area {
  margin-top: -20px;
  padding: 50px 0;
  height:450px;
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
  background: url("../../assets/liked.png") no-repeat 6px 8px;
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