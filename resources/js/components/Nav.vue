<template>
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Rounded:opsz,wght,FILL,GRAD@48,400,0,0" />
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@48,400,0,0" />

    <aside :class="`${is_expanded ? 'is-expanded' : ''}`">
		<h3>Menu</h3>
		<div class="menu">
			<router-link to="/" class="button">
				<span class="material-symbols-rounded">home</span>
				<span class="text">Home</span>
			</router-link>
			<router-link to="/about" class="button">
				<span class="material-symbols-rounded">description</span>
				<span class="text">About</span>
			</router-link>
			<router-link to="/team" class="button">
				<span class="material-symbols-rounded">group</span>
				<span class="text">Team</span>
			</router-link>
			<router-link to="/contact" class="button">
				<span class="material-symbols-outlined">admin_panel_settings</span>
				<span class="text">Administration</span>
			</router-link>
		</div>

		<div class="flex"></div>


		<div class="menu">
			<router-link to="/settings" class="button ">
				<span class="material-symbols-rounded">settings</span>
				<span class="text">Settings</span>
			</router-link>
		</div>

        <div class="menu-toggle-wrap">
			<button class="menu-toggle" @click="ToggleMenu">
				<span class="material-symbols-outlined menu-icon">menu</span>
                <span class="material-symbols-outlined arrow-back">arrow_back</span>
			</button>
		</div>



	</aside>
</template>


<script setup>
import { Menu, MenuButton, MenuItems, MenuItem } from '@headlessui/vue'

import {ref} from 'vue'


const is_expanded = ref(localStorage.getItem("is_expanded") === "true")
const ToggleMenu = () => {
	is_expanded.value = !is_expanded.value
	localStorage.setItem("is_expanded", is_expanded.value)
}


</script>



<style lang="scss" scoped>




aside {
	display: flex;
	flex-direction: column;
	background-color: var(--dark);
	color: var(--light);
	width: calc(2rem + 32px);
	overflow: hidden;
	min-height: calc(100vh - 5vh);
	padding: 1rem;
	transition: 0.2s ease-in-out;

	.flex {
		flex: 1 1 0%;
	}

	.menu-toggle-wrap {
		display: flex;
		justify-content: flex-end;
		margin-bottom: 1rem;
		position: relative;
		top: 0;
		transition: 0.2s ease-in-out;
        .arrow-back { display: none; }
        .settings-icon {display: none;}
		.menu-toggle {
			transition: 0.2s ease-in-out;
			.material-symbols-rounded, .material-symbols-outlined {
				font-size: 2rem;
				color: var(--light);
				transition: 0.2s ease-out;
			}

			&:hover {
				.material-symbols-rounded, .material-symbols-outlined {
					color: var(--primary);

				}
			}
		}
	}
	h3, .button .text {
		opacity: 0;
		transition: opacity 0.3s ease-in-out;
	}
	h3 {
		color: var(--grey);
		font-size: 0.875rem;
		margin-bottom: 0.5rem;
		text-transform: uppercase;
	}
	.menu {
		margin: 0 -1rem;
		.button {
			display: flex;
			align-items: center;
			text-decoration: none;
			transition: 0.2s ease-in-out;
			padding: 0.5rem 1rem;
			.material-symbols-rounded, .material-symbols-outlined {
				font-size: 2rem;
				color: var(--light);
				transition: 0.2s ease-in-out;
			}
			.text {
				color: var(--light);
				transition: 0.2s ease-in-out;
			}
			&:hover {
				background-color: var(--dark-alt);
				.material-symbols-rounded, .material-symbols-outlined, .text {
					color: var(--primary);
				}
			}
			&.router-link-exact-active {
				background-color: var(--dark-alt);
				border-right: 5px solid var(--primary);
				.material-symbols-rounded,.material-symbols-outlined,  .text {
					color: var(--primary);
				}
			}
		}
	}
	.footer {
		opacity: 0;
		transition: opacity 0.3s ease-in-out;
		p {
			font-size: 0.875rem;
			color: var(--grey);
		}
	}
	&.is-expanded {
		width: var(--sidebar-width);
		.menu-toggle-wrap {
			top: 0;

        .menu-icon { display: none; }
        .arrow-back { display: inline-block; }

            .settings-icon{
            	display: inline-block;
            }

		}
		h3, .button .text {
			opacity: 1;
		}
		.button {
			.material-symbols-rounded, .material-symbols-outlined {
				margin-right: 1rem;
			}
		}
		.footer {
			opacity: 0;
		}
	}
	@media (max-width: 1024px) {
		position: absolute;
		z-index: 99;
	}
}




</style>

