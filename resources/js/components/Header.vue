<template>



<div class=" header border-2">
        <div class="menu-toggle-wrap">
			<button class="menu-toggle" @click="ToggleMenu">
				<span class="material-symbols-outlined menu-icon">menu</span>
                
			</button>
		</div>

</div>

</template>

<script>
export default {

}
</script>

<style lang="scss">

	.logo {
		margin: 1rem;
		img {
			width: 2rem;
		}
	}

.header {
    min-height: 5vh;
    min-width: 100%;
}

</style>
