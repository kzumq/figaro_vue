<template>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@48,400,0,0" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />


<div class=" header container">

    <ul class="headernav">
        <li class="menu-toggle-wrap ">

			<button class="menu-toggle" @click="toggle">
				<span class="material-symbols-outlined menu-icon">menu</span>
			</button>

        </li>
        <li class="profil">
            <ProfilDropDown />
        </li>
    </ul>
</div>

</template>

<script>
import ProfilDropDown from './ProfilDropDown.vue'
export default {
    data() {
        return {
            isActive: false,
            showMenu: false
        };
    },
    methods: {
        toggle() {
            this.isActive = !this.isActive;
            this.$emit("isActive", this.isActive);
        }
    },
    components: { ProfilDropDown }
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
    padding: 1rem;
    background-color: var(--dark);
    min-height: 5vh;
    min-width: 100%;
}

li {
    list-style-type: none;
}

li:first-child{
    float: left;

}

li:last-child {
    float: right;

}

</style>
