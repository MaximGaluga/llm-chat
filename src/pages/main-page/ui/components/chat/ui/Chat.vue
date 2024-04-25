<template>
	<div class="chat-wrapper">
		<div class="chat-field">
			<div class="chat">
				12312
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
	flex-basis: 70%;
}

.input-wrapper
{
	grid-area: input;
	display: flex;
	justify-content: center;
	margin-bottom: 50px;
}
</style>