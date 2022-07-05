<template>
  <div>
    <div class="relative">
      <!-- Dropdown toggle button -->

        <button @click="isOpen" class="flex menu-toggle" style="margin-right: 1rem;"  >
            <span class="material-symbols-outlined" >notifications</span>
        </button>


      <!-- Dropdown menu -->
      <div v-show="show" class="absolute right-0  bg-white rounded-md shadow-xl  w-44" style="margin: 0.5rem 1rem 0 0;">
        <router-link to="/" class="block px-4 py-2 text-sm text-black  hover:bg-indigo-400 hover:text-indigo-100">

        </router-link>
        <router-link
          to="/"
          class="block px-4 py-2 text-sm text-indigo-100  hover:bg-indigo-400 hover:text-indigo-100"
        >
          Dropdown List 2
        </router-link>
        <router-link
          to="/"
          class="block px-4 py-2 text-sm text-indigo-100  hover:bg-indigo-400 hover:text-indigo-100"
        >
          Dropdown List 3
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

    .menu-toggle {
            .material-symbols-outlined {
                font-size: 2rem;
                color: var(--light);
                margin: 8px;
                padding: 8px;

            }
            &:hover {
                .material-symbols-outlined {
                    color: var(--primary);
                    background-color: #2e2e2e;
                    border: 1px;
                    border-radius: 50%;

                }
            }
        }

</style>
