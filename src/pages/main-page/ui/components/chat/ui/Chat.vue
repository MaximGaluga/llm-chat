<script setup lang="ts">
import { Message } from './components'


</script>

<template>
	<div class="chat-wrapper">
		<div class="chat-field">
			<div class="chat">
				<Message :text="'123'" isUser />
				<Message :text="'123'" v-for="a in 100" />
			</div>
		</div>
		<div class="input-wrapper">
			<div>
				<a-input-search
					placeholder="Your promt starts here..."
					enter-button
					style="width: 500px"
					size="large"
				/>
			</div>
		</div>
	</div>
</template>

<style scoped lang="scss">
.chat-wrapper
{
	margin-top: 15px;
	display: grid;
	grid-template:
		'chat' 1fr
		'input' auto
		/ 1fr;
}

.chat-field
{
	grid-area: chat;
	display: flex;
	justify-content: center;
}

.chat
{
	display: flex;
	flex-direction: column;
	gap: 10px;
	flex-basis: 70%;
	height: 80vh;
	overflow-y: auto;
	padding: 15px;
}

.input-wrapper
{
	grid-area: input;
	display: flex;
	justify-content: center;
	margin-bottom: 50px;
}
</style>