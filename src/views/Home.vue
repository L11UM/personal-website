<template>
  <div class="container">
    <div id="name-container">
      <img id="avatar" src="./../assets/images/av.png" alt="avatar" />
      <h1>Liam Thompson</h1>
    </div>
    <div class="title-desc-container">
      <a id="github" href="https://github.com/L11UM" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/github.svg" />Developer</a
      >
      <span>/</span>
      <a id="sspai" href="https://sspai.com/u/spencerwoo/posts" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/sspai.svg" />Writer</a
      >
      <span>/</span>
      <a id="blog" href="https://blog.spencerwoo.com" target="_blank" rel="noopener noreferrer"
        ><img class="title-font" src="./../assets/images/zeit.svg" />Blogger</a
      >
    </div>
    <div class="article">
      <h2>Welcome</h2>
      <p>
        I'm <i>Liam</i> or
        <a href="https://twitter.com/L3AWM" target="_blank" rel="noopener noreferrer">@L3AWM</a> /
        <a href="https://weibo.com/spencerwoo" target="_blank" rel="noopener noreferrer">@liambthompson</a> /
        <a href="https://github.com/l11um" target="_blank" rel="noopener noreferrer">@liium</a>. 
        This site is a directory for my notes and creative work
      </p>

      <h2>Links and things I'm working on</h2>
      <ul>
        <li>
          <a href="https://www.youtube.com/channel/UCK231EtrX0-zU0vLuaaDKCg" target="_blank" rel="noopener noreferrer">Treys Youtube Channel</a>)
          <i
            ><a
              href="https://github.com/L11UM"
              target="_blank"
              rel="noopener noreferrer"
              >My Code</a
            ></i>
        </li>
        <li>
          🍭 BIT Alumni (🇨🇳
          <a href="" target="_blank" rel="noopener noreferrer">35mm Photography</a
          >), <i>BSc in CS</i>.
        </li>
        <li>🔭 <b></b></li>
      </ul>

      <h2>Devices</h2>
      <ul>
        <li>⚫ ThinkPad X1 Carbon 7th Gen</li>
        <li>🔵 iPhone 12 / iPad Air 3 / AirPods Pro</li>
      </ul>

      <h2>How can we trust you!</h2>
      <p>
        I have verified my identity with a GPG signature which proves my ownership of this domain. (See the cryptography
        proof here:
        <a
          href="http://keybase.io/spencerwoo/sigchain#abb6f40f8c804e7411e91544b7cdb8e011df8e6f84dcd0b709f848f85dc6248d0f"
          target="_blank"
          rel="noopener noreferrer"
          >Keybase - claimed ownership of <b>spencerwoo.com</b> via dns</a
        >.) In other words, <i>I AM LEGIT HERE.</i>
      </p>
      <p>
        I have my GPG public key hosted on
        <a href="http://keybase.io/spencerwoo" target="_blank" rel="noopener noreferrer">Keybase - spencerwoo</a>. You
        can pull and import my GPG public key with:
      </p>
      <pre>curl https://keybase.io/spencerwoo/pgp_keys.asc | gpg --import</pre>

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
