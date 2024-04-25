<script setup lang="ts">
const history = [1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, 1, 2, 3, 4, ];
</script>

<template>
	<div class="history-wrapper">
		<div class="history-content" v-for="(item, index) in history" :key="index"> 
			<div class="history-content-wrapper">
				{{ item }}
			</div>
		</div>
	</div>
</template>

<style scoped lang="scss">
.history-wrapper
{
	display: flex;
	flex-direction: column;
	width: 400px;
	border-right: 2px solid gray;
	height: 100vh;
	overflow-y: auto;
}
.history-content
{
	flex-shrink: 0;
	height: 100px;
	border-bottom: 1px solid gray;
}
.history-content-wrapper
{
	display: flex;
	justify-content: center;
	align-items: center;
}
</style>