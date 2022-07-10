<template>
  <div>
    <div class="relative">
      <!-- Dropdown toggle button -->

        <button @click="isOpen" class="flex menu-toggle-not" style="margin-right: 1rem;"  >
            <span class="material-symbols-outlined material-symbols-outlined-not" >notifications</span>
        </button>


      <!-- Dropdown menu -->
      <div v-show="show" class="z-[1000] absolute right-0 notification drop-shadow-lg " style="margin: 1rem 1rem 0 0;">

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

    .notification {
        background-color: white;
        width: 16rem;
        height: 16rem;
    }

    .menu-toggle-not {
            .material-symbols-outlined-not {
                font-size: 1rem;
                color: var(--light);


            }
            &:hover {
                .material-symbols-outlined-not {
                    color: var(--primary);
                }
            }
        }

</style>
