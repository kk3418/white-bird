<script setup>
import { ref } from "vue";
const isSelected = ref(0);
const isExpand = ref(false);

const handleClick = (v) => {
  isSelected.value = v;
};

const handleExpand = () => {
  isExpand.value = !isExpand.value;
};
</script>
<template>
  <div class="menu">
    <div class="menu-header">
      <img
        class="hamburger"
        v-show="!isExpand"
        src="../assets/hamburger-icon.png"
        alt=""
        @click="handleExpand"
      />
      <img
        class="hamburger"
        v-show="isExpand"
        src="../assets/cancel.png"
        alt=""
        @click="handleExpand"
      />
      <h2 class="title">白頭翁不吃小米</h2>
    </div>
    <ul :class="['menu-list', { expand: isExpand }]">
      <li
        :class="['menu-item', { selected: isSelected === 0 }]"
        @click="handleClick(0)"
      >
        白頭翁的特性
      </li>
      <li
        :class="['menu-item', { selected: isSelected === 1 }]"
        @click="handleClick(1)"
      >
        白頭翁的故事
      </li>
      <li
        :class="['menu-item', { selected: isSelected === 2 }]"
        @click="handleClick(2)"
      >
        白頭翁的美照
      </li>
      <li
        :class="['menu-item', { selected: isSelected === 3 }]"
        @click="handleClick(3)"
      >
        白頭翁的危機
      </li>
    </ul>
  </div>
</template>
<style scoped>
.menu {
  width: 24vw;
  background-color: #fff;
}
.menu-header {
  display: flex;
  justify-content: center;
  align-items: center;
}
.title {
  font-size: 1.875rem;
  font-weight: 700;
  line-height: 2.55rem;
  margin: 7.8vh auto 7.55vh auto;
  cursor: default;
}
.menu-list {
  text-decoration: none;
  list-style-type: none;
  padding: 0;
  margin: 0;
  text-align: center;
}
.menu-item {
  margin-bottom: 2.17vh;
  cursor: pointer;
  line-height: 1.53rem;
}
.menu-item:last-child {
  margin-bottom: 0;
}
@media (max-width: 750px) {
  .menu {
    width: 100vw;
  }
  .menu-header {
    height: 8.43vh;
  }
  .title {
    font-size: 1.25rem;
    line-height: 1.7rem;
    margin: 0 13.3vw 0 17.9vw;
  }
  .menu-list {
    height: 0;
    transform: scale(0);
    transform-origin: top;
    transition: all 0.3s ease-in-out;
  }
  .menu-list.expand {
    padding-bottom: 3.65vh;
    height: auto;
    transform: scale(1);
    transform-origin: top;
    transition: all 0.3s ease-out;
  }
}
</style>
