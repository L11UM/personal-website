<template>
  <div class="container">
    <div id="name-container">
      <img id="avatar" src="./../assets/images/av.png" alt="avatar" />
      <h1>Liam Thompson</h1>
    </div>
    <div class="title-desc-container">
      <a id="github" href="https://github.com/L11UM" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/github.svg" />Develop</a
      >
      <span>/</span>
      <a id="sspai" href="https://medium.com/@liambt20" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/sspai.svg" />Write</a
      >
      <span>/</span>
      <a id="blog" href="https://blog.spencerwoo.com" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/zeit.svg" />Art</a
      >
    </div>
    <div class="article">
      <h2>Welcome</h2>
      <p>
        I'm <i>Liam</i> or
        <a href="https://twitter.com/L3AWM" target="_blank" rel="noopener noreferrer">@L3AWM</a> /
        <a href="https://www.instagram.com/liambthompson/" target="_blank" rel="noopener noreferrer">@liambthompson</a> /
        <a href="https://github.com/l11um" target="_blank" rel="noopener noreferrer">@liium</a>. 
       <br> This site is a directory for my notes and creative work 
      </p>

      <h2>Links and things I'm working on</h2>
      <ul>
        <li>
          <a href="https://www.youtube.com/channel/UCK231EtrX0-zU0vLuaaDKCg" target="_blank" rel="noopener noreferrer">Trey's Youtube Channel</a>
          <li>
            <a href="https://github.com/L11UM" target="_blank" rel="noopener noreferrer">My Code</a
            ></li>
        </li>
        <li>
          <a href="" target="_blank" rel="noopener noreferrer">35mm Photography</a> <i>Site coming soon..</i>
        </li>
         <li>
          <a href="https://www.twitch.tv/liambingus" target="_blank" rel="noopener noreferrer">Twitch</a>
        </li>
        <li>
          <a href="https://docs.google.com/document/d/195gGzkvd_VNd6eX9-eIUYu0k-QOsIBmIhp0RiAuIvkI/edit?usp=sharing" target="_blank" rel="noopener noreferrer">My Resume</a>
        </li>
      </ul>

      <h2>Setup</h2>
      <ul>
        <li>⚫ Custom Built PC:</li>
        <li>AMD FX(tm)-8300 Eight-Core Processor</li>
        <li>NVIDIA GTX 1050</li>
        <li>MS970 MoBO</li> 
        
        <li>🔵 VSCode Configuration</li>
      </ul>

      <h2>Freelance work:</h2>
      <p>
        I offer web/UI devolpment services for low prices!</p>
      
        <a href="https://github.com/L11UM" target="_blank" rel="noopener noreferrer">You can take a look at some of my work here</a>

        <!--Contact-->
      <h2>Contact Me</h2>
      <ul>
        <li>
          <b>Email:</b>
          <a href="mailto:liambt20@gmail.com">liambt20#gmail.com</a><i> (Preferred)</i>
        </li>
        <li>
          <b>Phone #</b>
          480-828-1953
        </li>
      </ul>
    </div>
  </div>
</template>
    <!--CSS-->
<style lang="css" scoped>
#name-container {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
}

#avatar {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  margin-right: 12px;
}

#copyright:hover {
  border: none;
}

.title-font {
  width: 16px;
  height: 16px;
  margin-right: 4px;
}

.title-desc-container {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  margin: 8px 0;
}

.title-desc-container a {
  display: flex;
  align-items: center;
}

.title-desc-container span {
  margin: 0px 4px;
}

.title-desc-container #github {
  color: #24292e;
}

.title-desc-container #sspai {
  color: #ca2c2a;
}

.title-desc-container #blog {
  color: #0070f3;
}
</style>
