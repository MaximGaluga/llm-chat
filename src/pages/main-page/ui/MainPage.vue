<script setup lang="ts">
import { History } from './components'
import { Chat } from './components'

</script>

<template>
	<div class="main-page-wrapper">
		<History style="grid-area: history;" />
		<Chat style="grid-area: chat;" />
	</div>
</template>

<style scoped lang="scss">
.main-page-wrapper
{
	display: grid;
	grid-template:
		'history chat'
		/ auto 1fr;
	width: 100%;
}
</style>