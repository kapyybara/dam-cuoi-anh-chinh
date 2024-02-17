<script setup lang="ts">
import { STORIES } from '../../../constants';
</script>

<template>
	<div class="stories">
		<div class="title">
			<div class="title__content">Chuyện Tình Của Chính & Huyền</div>
			<span class="title__decor">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="333"
					height="41"
					viewBox="0 0 333 41"
					fill="none"
				>
					<path
						d="M330 12.526C262.372 9.93298 195.326 5.09811 127.574 4.02213C88.6295 3.40364 -27.835 1.59314 10.7146 5.08509C74.0777 10.8247 139.564 10.6403 203.361 14.5001C228.08 15.9956 252.6 18.0002 277.193 20.1187C286.657 20.934 294.049 22.3117 278.905 21.7891C211.313 19.4567 144.072 14.2733 76.4786 11.7667C69.2655 11.4992 47.8946 11.3688 54.8425 12.6019C80.3101 17.1216 107.632 18.9022 133.686 21.4095C165.06 24.4287 196.941 26.3143 228.054 30.293C239.23 31.7222 254.198 32.1681 264.603 35.0764C283.015 40.2229 224.282 37.0577 204.095 36.8227C170.498 36.4317 136.939 35.2271 103.371 34.3931"
						stroke="#C79272"
						stroke-width="5"
						stroke-linecap="round"
					/>
				</svg>
			</span>
		</div>
		<div class="slide">
			<div
				class="slide__item"
				v-for="(story, index) in STORIES"
				:key="index"
			>
				<img class="slide__item-img" :src="story.img" alt="" />
				<span class="slide__item-time">{{ story.time }}</span>
			</div>
		</div>
	</div>
</template>

<style lang="scss" scoped>
.stories {
	padding-top: 60px;

	width: 100%;
	height: 100%;
	background: #fff;
	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: start;
}

.title {
	position: relative;
	width: fit-content;
	margin-bottom: 60px;

	&__content {
		color: #191919;

		text-align: center;
		font-family: 'Berfilem';
		font-size: 50px;
		font-style: normal;
		font-weight: 400;
		line-height: 54px; /* 108% */
		letter-spacing: 1.5px;
		text-transform: capitalize;
	}

	&__decor {
		position: absolute;
		right: 0;
		bottom: 0;
		transform: translateY(100%);
	}
}
</style>
