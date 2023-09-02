<script setup></script>
<template>
  <div class="container">
    <div class="banner">
      <div class="banner-content">
        <h1 class="banner-title">白頭翁 (Chinese bulbul)</h1>
        <p class="banner-description">
          又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10
          年。
        </p>
      </div>
    </div>
    <div class="content">
      <section>
        <h2 class="title">外觀</h2>
        <p>
          白頭鵯體長約17到22公分，額至頭頂純黑色而富有光澤，兩眼上方至後枕白色，形成一白色枕環。耳羽後部有一白斑，此白環與白斑在黑色的頭部均極為醒目，老鳥的枕羽(後頭部)更潔白，所以又叫「白頭翁」。
        </p>
      </section>
      <section>
        <h2 class="title">棲地</h2>
        <p>
          白頭翁和麻雀、綠繡眼合稱「城市三寶」，常成群出現在平原區灌木叢、丘陵樹林地帶，以及校園、公園、庭院、行道中的各種高高的電線與樹上。
        </p>
      </section>
      <section>
        <h2 class="title">食性</h2>
        <p>
          以果樹的漿果和種子為主食，並時常飛入果園偷吃果實，還會吃嫩葉嫩芽，尤其是胡蝶蘭的嫩葉嫩芽葉，偶爾啄食昆蟲。
        </p>
      </section>
    </div>
  </div>
</template>
<style scoped>
.container {
  min-height: 100vh;
}
.banner {
  position: relative;
  width: 76vw;
  height: calc(76vw * 0.579);
  background-image: url("../assets/banner.png");
  background-position: top left;
  background-size: cover;
  background-repeat: no-repeat;
  overflow: hidden;
  color: #fff;
}
.banner-content {
  position: absolute;
  right: 3.11vw;
  bottom: 3.68vh;
  width: 45vw;
  text-align: right;
}
.banner-title {
  font-size: 3rem;
  font-weight: 700;
  line-height: 4.086rem;
  margin: 0 0 0.25rem 0;
}
.banner-description {
  font-size: 1.125rem;
  line-height: 1.533rem;
}
.content {
  width: 76vw;
  min-height: 22.46vh;
  padding: 5.8vh 3.5vw 8.38vh 3.5vw;
  box-sizing: border-box;
  display: flex;
  justify-content: space-evenly;
  flex-wrap: nowrap;
  column-gap: 5.48vw;
}
section {
  display: flex;
  align-items: flex-start;
  width: 19.34vw;
}
.title {
  position: relative;
  writing-mode: vertical-rl;
  text-orientation: upright;
  font-size: 2.25rem;
  font-weight: 700;
  line-height: 2.5rem;
  margin: 0 2.63vw 0 0;
}
.title::after {
  position: absolute;
  bottom: -0.9rem;
  right: -0.8rem;
  width: 1.56rem;
  height: 1.56rem;
  box-sizing: border-box;
  border-radius: 50%;
  border: 0.5rem solid #aa666699;
  content: "";
}
@media (max-width: 750px) {
  .banner {
    width: 100vw;
    height: calc(100vw * 0.83);
  }
  .banner-content {
    width: 88vw;
    right: 7.19vw;
    bottom: 2.31vh;
  }
  .banner-title {
    line-height: 3.125rem;
    margin-bottom: 0.58rem;
  }
  .content {
    padding: 7.92vh 0 6.91vh 0;
    width: 100vw;
    flex-wrap: wrap;
    row-gap: 7.86vh;
  }
  section {
    width: 80.6vw;
    height: auto;
  }
  .title {
    margin-right: 10.09vw;
  }
}
</style>
