<template>
  <div>
    <div class="relative">
      <!-- Dropdown toggle button -->
      <button @click="isOpen" class="flex menu-toggle" style="margin-right: 1rem;" >
        <img src="../../../public/assets/img/person.png" class="rounded-full h-8 w-8"  alt="">
      </button>

      <!-- Dropdown menu -->
      <div v-show="show" class="absolute right-0 profil-dropdown drop-shadow-lg rounded w-44" style="margin: 1rem 1rem 1rem 0;">
        <router-link to="/" class="flex  items-center px-4 py-2 text-sm text-black  ">
            <img src="../../../public/assets/img/person.png" class="rounded-full h-10 w-10 justify-start" style="margin: 1rem"  alt="">
            <h2 class="items-center justify-end">Figaro</h2>

            </router-link>
        <hr>
        <router-link
          to="/"
          class="flex px-4 py-2 text-sm items-center profil-dropdown-items" style="margin-top: 1rem "
        >
        <span class="material-symbols-outlined items-center justify-start">person</span>
        <h4 class="items-center justify-end " style="margin-left: 1rem;">  Mein Profil </h4>

        </router-link>
        <router-link
          to="/"
          class="flex px-4 py-2 text-sm items-center profil-dropdown-items"
        >
        <span class="material-symbols-outlined items-center justify-start">group</span>
        <h4 class="items-center justify-end profil-dropdown-icons" style="margin-left: 1rem;">  Mein Team </h4>
        </router-link>
        <router-link
          to="/"
          class="flex px-4 py-2 text-sm items-center profil-dropdown-items"
        >
        <span class="material-symbols-outlined items-center justify-start">logout</span>
        <h4 class="items-center justify-end profil-dropdown-icons" style="margin:0 0 0 1rem">  logout </h4>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from 'vue';
  export default {
    setup() {
      let show = ref(false);
      const isOpen = () => (show.value = !show.value);
      return { show, isOpen };
    },
  };
</script>

<style lang="scss">

.profil-dropdown-icons {

}

hr {

    width: 100%;
    border-color: rgb(187, 187, 187);

}

.profil-dropdown {
    background-color: white;
    width: 16rem;
    height: 16rem;

    .profil-dropdown-items {
        padding: 1rem;
        color: black;
        &:hover {
        color: var(--primary);
        }
    }
}

</style>
