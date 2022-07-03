<template>
    <div class="menu-item" @click="isOpen = !isOpen" >
        <button class="menu-btn" style="width: 2rem; heigth: 2rem">
        <img src="../../../public/assets/img/person.png" alt=""></button>
        <transition name="fade" apear>
         <div class="sub-menu" v-if="isOpen">
            <div class="menu-item">
              <router-link to="/services/web">Web</router-link>
            </div>
            <div class="menu-item">
              <router-link to="/services/design">Design</router-link>
            </div>
            <div class="menu-item">
              <router-link to="/services/videos">Videos</router-link>
            </div>
        </div>
        </transition>
    </div>
</template>

<script>
export default {
  name: 'services',
  data () {
    return {
      isOpen: false,
      }
    }
}
</script>

<style>

nav .menu-item .sub-menu {
  position: absolute;
  background-color: #222;
  top: calc(100% + 5px);
  left: 50%;
  transform: translateX(-50%);
  width: max-content;
}
.fade-enter-active,
.fade-leave-active {
  transition: all .5s ease-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.sub-menu {
  cursor: pointer;
}

</style>
