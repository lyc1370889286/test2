<template>
  <body>
  <div class="logo">
    <h1>评论</h1>
    <h2>E</h2>
  </div>
  <nav id="sort">
    <ul>
      <li><a href="/editcomment"><img src="assets/images/icon-1.png" alt=""> <em>编辑</em></a></li>
      <li><a href="/history"><img src="assets/images/icon-2.png" alt=""> <em>按时间</em></a></li>
      <li><a href="/science"><img src="assets/images/icon-3.png" alt=""> <em>按点赞数</em></a></li>
    </ul>
  </nav>

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
              <li><a href="/alla">所有文章</a></li>
              <li><a href="/myarticle">我的文章</a></li>
              <li><a href="/mycomment">我的评论</a></li>
              <li><a href="/personalkeep">个人中心</a></li>
            </ul>
          </div>
        </nav>
        <!-- End of Main Navigation -->

      </div>
    </header>
  </div>

  <div class="row separator">
    <section class="span4 articles-list">
      <h3>我的评论</h3>
      <button @click="hold">保存</button>
      <ul class="articles">
        <li class="article-entry standard">
          <h4><a href="single.html">Integrating WordPress with Your Website</a></h4>
          <span class="article-meta">25 Feb, 2013 in <a href="#" title="View all posts in Server &amp; Database">Server &amp; Database</a></span>
          <span class="like-count">66</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">WordPress Site Maintenance</a></h4>
          <span class="article-meta">24 Feb, 2013 in <a href="#" title="View all posts in Website Dev">Website Dev</a></span>
          <span class="like-count">15</span>
          <button>删除</button>
        </li>
        <li class="article-entry video">
          <h4><a href="single.html">Meta Tags in WordPress</a></h4>
          <span class="article-meta">23 Feb, 2013 in <a href="#" title="View all posts in Website Dev">Website Dev</a></span>
          <span class="like-count">8</span>
          <button>删除</button>
        </li>
        <li class="article-entry image">
          <h4><a href="single.html">WordPress in Your Language</a></h4>
          <span class="article-meta">22 Feb, 2013 in <a href="#" title="View all posts in Advanced Techniques">Advanced Techniques</a></span>
          <span class="like-count">6</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">Know Your Sources</a></h4>
          <span class="article-meta">22 Feb, 2013 in <a href="#" title="View all posts in Website Dev">Website Dev</a></span>
          <span class="like-count">2</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">Validating a Website</a></h4>
          <span class="article-meta">21 Feb, 2013 in <a href="#" title="View all posts in Website Dev">Website Dev</a></span>
          <span class="like-count">3</span>
          <button>删除</button>
        </li>
      </ul>
    </section>


    <section class="span4 articles-list">
      <ul class="articles">
        <li class="article-entry standard">
          <h4><a href="single.html">Integrating WordPress with Your Website</a></h4>
          <span class="article-meta">25 Feb, 2013 in <a href="#" title="View all posts in Server &amp; Database">Server &amp; Database</a></span>
          <span class="like-count">66</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">Using Javascript</a></h4>
          <span class="article-meta">25 Feb, 2013 in <a href="#" title="View all posts in Advanced Techniques">Advanced Techniques</a></span>
          <span class="like-count">18</span>
          <button>删除</button>
        </li>
        <li class="article-entry image">
          <h4><a href="single.html">Using Images</a></h4>
          <span class="article-meta">25 Feb, 2013 in <a href="#" title="View all posts in Designing in WordPress">Designing in WordPress</a></span>
          <span class="like-count">7</span>
          <button>删除</button>
        </li>
        <li class="article-entry video">
          <h4><a href="single.html">Using Video</a></h4>
          <span class="article-meta">24 Feb, 2013 in <a href="#" title="View all posts in WordPress Plugins">WordPress Plugins</a></span>
          <span class="like-count">7</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">WordPress Site Maintenance</a></h4>
          <span class="article-meta">24 Feb, 2013 in <a href="#" title="View all posts in Website Dev">Website Dev</a></span>
          <span class="like-count">15</span>
          <button>删除</button>
        </li>
        <li class="article-entry standard">
          <h4><a href="single.html">WordPress CSS Information and Techniques</a></h4>
          <span class="article-meta">24 Feb, 2013 in <a href="#" title="View all posts in Theme Development">Theme Development</a></span>
          <span class="like-count">1</span>
          <button>删除</button>
        </li>
      </ul>
    </section>
  </div>
  </body>
</template>

<script>
export default {
  name: "editComment",
  methods:{
    hold(){
      this.$router.push('myComment');
    }
  }
}
</script>

<style scoped>
#sort {
  top: 15%;
  text-align: center;
  background: rgba(0, 0, 0, 0.75);
  position: fixed;
  z-index: 100;
  height: 90%;
  left: 0;
  width: 15%;
  font-weight: 300;
  font-size: 1rem;
}
#sort em {
  font-style: normal;
  font-size: 13px;
  text-transform: uppercase;
  display: block;
  margin-top: 15px;
  color: #fff;
}

#sort ul li a {
  text-align: center;
}

#sort ul {
  position: relative;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  text-align: left;
  list-style-type: none;
  height: 70%;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-orient: vertical;
  -webkit-box-direction: normal;
  -ms-flex-direction: column;
  flex-direction: column;
  -ms-flex-pack: distribute;
  justify-content: space-around;
}
#sort ul li {
  text-align: center;
  margin: 5px 0px;
}
#sort a, #sort a:visited, #sort a:active {
  color: #fff;
}
#sort a {
  text-decoration: none!important;
  display: inline-block;
  width: 140px;
  padding: 15px 0px;
  position: relative;
  z-index: 0;
  transition: all .5s;
}
#sort a.active {
  background-color: rgba(0,0,0,0.8);
}
#sort a::before {
  content: "";
  position: absolute;
  height: 0%;
  width: 0%;
  bottom: 0;
  left: 0;
  opacity: 1;
  z-index: -1;
}
.logo {
  margin-top: 0px;
  top: 0;
  left: 0;
  z-index: 999999;
  position: fixed;
  display: inline-block;
  text-align: center;
  background-color: #faf5b2;
  height: 15%;
  width: 15%;
}
.logo h1 {
  font-size: 24px;
  text-transform: uppercase;
  font-weight: 900;
  color: #111;
  top: 50%;
  left: 50%;
  position: absolute;
  transform: translate(-50%, -50%);
}
.logo h2 {
  display: none;
}
body {
  background-color: #fff;
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
  height: auto !important;
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