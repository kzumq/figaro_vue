<template>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@48,400,0,0" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />


<nav class="flex items-center justify-between flex-wrap header">
    <div class="menu-toggle-wrap items-center" style="margin: 1rem 0 0 1rem ;">
        <button class="menu-toggle" @click="toggle">
		    <span class="material-symbols-outlined menu-icon">menu</span>
		</button>
    </div>

    <div class="items-center">
        <Notifications  />
    </div>
    <div class="items-center">
        <ProfilDropDown />
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
        }
        &:hover {
			.material-symbols-outlined {
				color: var(--primary);
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
