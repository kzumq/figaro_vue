<template>



<div class=" header border-2">
        <div class="menu-toggle-wrap">
			<button class="menu-toggle" v-on:click="toggle">
				<span class="material-symbols-outlined menu-icon">menu</span>
			</button>
		</div>

</div>

</template>

<script>
export default {
    data()  {
        return {
            isActive: false
        }
    },
    methods: {
        toggle() {
            this.isActive = !this.isActive
            this.$emit('isActive', this.isActive)
        }
    }
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
