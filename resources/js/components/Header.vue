<template>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@48,400,0,0" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />


<nav class="flex items-center justify-between flex-wra header">
    <div class="menu-toggle-wrap">
        <button class="menu-toggle" @click="toggle">
		    <span class="material-symbols-outlined menu-icon">menu</span>
		</button>
        </div>
    <div class="flex items-center flex-no-shrink text-white mr-6">
        <svg class="h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" xmlns="http://www.w3.org/2000/svg"><path d="M13.5 22.1c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05zM0 38.3c1.8-7.2 6.3-10.8 13.5-10.8 10.8 0 12.15 8.1 17.55 9.45 3.6.9 6.75-.45 9.45-4.05-1.8 7.2-6.3 10.8-13.5 10.8-10.8 0-12.15-8.1-17.55-9.45-3.6-.9-6.75.45-9.45 4.05z"/></svg>
        <span class="font-semibold text-xl tracking-tight">Tailwind CSS</span>
    </div>
    <div class="block lg:hidden">
        <button class="flex items-center px-3 py-2 border rounded text-teal-lighter border-teal-light hover:text-white hover:border-white">
            <svg class="h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
        </button>
    </div>
    <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
        <div class="text-sm lg:flex-grow">
            <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-lighter hover:text-white mr-4">Docs</a>
            <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-lighter hover:text-white mr-4">Examples</a>
            <a href="#responsive-header" class="block mt-4 lg:inline-block lg:mt-0 text-teal-lighter hover:text-white">Blog</a>
        </div>
        <div style="margin-right: 2rem;">
            <Notifications  />
        </div>
        <div>
            <ProfilDropDown />
        </div>
    </div>
</nav>


</template>

<script>
import ProfilDropDown from './ProfilDropDown.vue'
import Notifications from './Notifications.vue';
export default {
    data() {
        return {
            isActive: false,
            isOpen: false,
        };
    },
    methods: {
        toggle() {
            this.isActive = !this.isActive;
            this.$emit("isActive", this.isActive);
        }
    },
    components: { ProfilDropDown, Notifications }
}
</script>

<style lang="scss">

.menu-toggle-wrap {
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

}


.header {
    background-color: var(--dark);
    min-height: 5vh;
    min-width: 100%;

}

</style>
