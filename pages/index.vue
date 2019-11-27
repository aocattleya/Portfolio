<template>
  <div class="container">
    <div class="profiles">
      <div class="profile">
        <img src="~/assets/ao.png" class="logo" />
        <h1 class="title">aocattleya</h1>
        <h2 class="subtitle">
          趣味でフロントエンドを主軸にWeb技術を学んでいます。
          <br />絵も描きます🎨
        </h2>
        <dev class="links">
          <a
            class="output_logo"
            href="https://github.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="output_logo"
            href="https://qiita.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="output_logo"
            href="https://twitter.com/aocattleya"
            target="_blank"
          ></a>
          <a
            class="output_logo"
            href="https://cattleya.hatenablog.com/"
            target="_blank"
          ></a>
          <a
            class="output_logo"
            href="https://connpass.com/user/aocattleya/"
            target="_blank"
          ></a>
        </dev>
        <div class="shooting_star"></div>
        <div class="shooting_star"></div>
        <div class="shooting_star"></div>
      </div>
    </div>
    <!-- <div class="project">
      <h2>PROJECT</h2>
      <div class="project">
        <img src="~/assets/timer.gif" class="project_gif" />
      </div>
    </div>-->
  </div>
</template>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  justify-content: center;
  align-items: center;
  text-align: center;
  max-width: 100%;
  height: 100%;
  object-fit: cover;
}

.profiles {
  width: 100%;
  height: 100vh;
}

.profile {
  position: absolute;
  left: calc(50% - 500px);
  top: calc(50% - 350px);
  width: 1000px;
  height: 700px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.logo {
  border-radius: 50%;
  width: 200px;
  box-shadow: 0 0 0 3px #fff, 0 0 0 4px #ccc, 0 2px 5px 4px rgba(0, 0, 0, 0.2);
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 500;
  font-size: 50px;
  padding: 10px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 20px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 10px;
  margin-bottom: 10px;
}

.links {
  width: 730px;
  margin: 0 auto;
  list-style: none;
  display: flex;
  border-top: 1px solid rgb(141, 141, 141);
  justify-content: space-around;
  padding-top: 30px;
  margin-bottom: 15px;
}

.output_logo {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  content: '';
  display: block;
  background-size: cover;
  background-position: center;
}

.output_logo:nth-child(1) {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  background: url('~assets/github.jpg');
  background-size: cover;
  background-position: center;
}

.output_logo:nth-child(2) {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  background: url('~assets/qiita.png');
  background-size: cover;
  background-position: center;
}

.output_logo:nth-child(3) {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  background: url('~assets/twitter.png');
  background-size: cover;
  background-position: center;
}

.output_logo:nth-child(4) {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  background: url('~assets/hatena.jpg');
  background-size: cover;
  background-position: center;
}

.output_logo:nth-child(5) {
  width: 100px;
  height: 100px;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
  background: url('~assets/connpass.png');
  background-size: cover;
  background-position: center;
}

.project {
  padding-top: 540px;
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 40px;
  color: #35495e;
  letter-spacing: 1px;
}
</style>
