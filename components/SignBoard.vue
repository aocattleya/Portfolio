<template>
  <div class="signboard">
    <div class="sign">作った物&実績</div>
    <div class="strings"></div>
    <div class="pin top"></div>
    <div class="pin left"></div>
    <div class="pin right"></div>
  </div>
</template>

<style scoped>
.signboard {
  position: absolute;
  top: 32px;
  right: 100px;
  width: 400px;
  height: 300px;
  margin-left: 500px;
  animation: swinging 4s ease-in-out infinite alternate;
  z-index: 1;
  opacity: 1;
  cursor: pointer;
}

.signboard .sign {
  position: absolute;
  top: 100px;
  left: 38px;
  bottom: 0;
  width: 80%;
  height: 150px;
  background: burlywood;
  border-radius: 15px;
  line-height: 175px;
  text-align: center;
  font-size: 40px;
  font-weight: 700;
  font-family: sans-serif;
  color: saddlebrown;
  text-shadow: 0 2px 0 rgba(255, 255, 255, 0.3), 0 -2px 0 rgba(0, 0, 0, 0.7);
  font-family: font;
  border-style: groove;
  border-color: burlywood;
}

.strings {
  position: absolute;
  top: 38px;
  left: 125px;
  width: 150px;
  height: 150px;
  border: 5px solid brown;
  transform: rotate(45deg);
  border-right: none;
  border-bottom: none;
}

.pin {
  position: absolute;
  width: 25px;
  height: 25px;
  border-radius: 50%;
}

.pin.top {
  background: gray;
  left: calc((400px - 25px) / 2);
}

.pin.right,
.pin.left {
  background: brown;
  top: 110px;
  box-shadow: 0 2px 0 rgba(255, 255, 255, 0.3);
}

.pin.left {
  left: calc((200px - 25px) / 2);
}

.pin.right {
  left: calc(200px + (200px - 25px) / 2);
}

@keyframes swinging {
  from {
    transform: rotate(10deg) translateX(-22px);
  }
  to {
    transform: rotate(-10deg) translateX(22px);
  }
}
</style>
