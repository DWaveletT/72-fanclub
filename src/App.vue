<template>
  <div class="full-container">
    <main class="main-container" id="particles-js">
      <div class="qq-group">
        <div class="logo-container-1">
          <div class="logo-container-2">
              <img class="avatar" src="/72-fanclub.png" />
          </div>
        </div>
        <div class="slogen">
          <div class="welcome">欢迎加入 Nanani 粉丝群</div>
          <div class="groupno" @click="copyNumber('167013550')">
            167013550
            <div class="copy">
              点击复制至剪贴板
            </div>
          </div>
        </div>
      </div>
    </main>

  </div>
</template>

<script setup lang="ts">

function copyNumber(qq: string){
  navigator.clipboard.writeText(qq);
}

</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 3em;
  background-color: black;

  margin: 0;
  padding: 1em 2em;
  
}

.full-container {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;
  
  background:
    radial-gradient(
      circle at 80% -10%,
      #D2FFED,
      transparent 80%
    ),
    #F7F7F7;
  
}

.main-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  width: 100%;
  flex-grow: 1;
}

.qq-group {
  max-height: 50%;

  display: flex;
  flex-direction: column;
  align-items: center;
}

.logo-container-1 {
  
  height: 25%;
  width: 25%;

  padding: 0.5em;

  background:
    radial-gradient(
      circle at 90% 10%,
      #EEEEEE,
      transparent 80%
    ),
    #F7F7F7;
  border-radius: 50%;
  overflow: hidden;
  z-index: 2;
}

.logo-container-2 {
  border-radius: 50%;
  overflow: hidden;
  z-index: 2;
}

.avatar {
  width: 100%;
  height: 100%;
  z-index: 2;

  user-select: none;

  transition: transform 10s ease-in-out;
  &:hover {
    transform: rotate(360deg);
  }
}

.slogen {
  z-index: 2;
}

.welcome {
  font-weight: 600;
  font-size: 300%;

  background-image: linear-gradient(to right, #CF00EB, #00B3EB);
	color: transparent;
	background-clip: text;

  text-align: center;
}

.groupno {
  font-weight: 300;
  font-size: 300%;

  background-image: linear-gradient(to right, #CF00EB, #00B3EB);
	color: transparent;
	background-clip: text;

  border-top: 2px solid #CF00EB;

  text-align: center;

  position: relative;

  cursor: pointer;

  &:hover {
    > .copy {
      opacity: 1;
    }
  }

  > .copy {
    opacity: 0;

    transition: opacity 0.3s ease-in-out;

    font-size: small;
    font-weight: normal;

    padding: 0.2em 0.8em;
    border-radius: 0.4em;

    display: block;
    position: absolute;
    bottom: -2em;

    left: 50%;

    transform: translateX(-50%);

    color: white;
    background-color: black;
  }
}

</style>
