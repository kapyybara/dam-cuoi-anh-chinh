<script setup lang="ts">
import HomeBanner from './Banner.vue';
import Stories from './Stories/index.vue'
</script>

<template>
	<div class="home">
		<img src="/us.png" alt="" />
		<HomeBanner />
		<div class="home-stories">
			<Stories />
		</div>
		<div class="home-wedding-images"></div>
		<div class="home-wedding-info container"></div>
		<div class="home-wedding-detail container"></div>
	</div>
</template>

<style lang="scss">
.home {
	width: 100%;
	height: fit-content;
	display: flex;
	flex-direction: column;
	align-items: center;
	gap: 24px;

	background: #fff;
	padding-top: 40px;

	&-stories {
		height: 1000px;
		width: 100%;
		background: blue;
	}

	&-wedding-images {
		height: 1000px;
		width: 100%;
		background: purple;
	}

	&-wedding-info {
		height: 1000px;
		width: 100%;
		background: red;
	}

	&-wedding-detail {
		height: 1000px;
		width: 100%;
		background: red;
	}
}

.container {
	margin: 0 60px;
	width: calc(100% - 120px) !important;
	@media only screen and (max-width: 768px) {
		margin: 0 12px;
		width: calc(100% - 24px) !important;
	}
}
</style>
