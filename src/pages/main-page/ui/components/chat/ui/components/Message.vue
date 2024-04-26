<script setup lang="ts">
import { PropType } from 'vue'

const props = defineProps({
	text: String as PropType<string>,
	isUser: Boolean as PropType<boolean>
});

</script>

<template>
	<div :class="['message-card', isUser ? 'user' : 'assistant']">
		<span :class="['text', isUser ? 'user' : 'assistant']">{{ text }}</span>
	</div>
</template>

<style scoped lang="scss">
.message-card
{
	display: flex;
	flex-direction: row;

	&.user {
		justify-content: flex-end;
	}

	&.assistant {
		justify-content: flex-start;
	}
}

.text
{
	border-radius: 5px;
	padding: 15px;
	
	&.user {
		background-color: rgba(239, 114, 231, 0.532);
	}

	&.assistant {
		background-color: rgba(114, 208, 239, 0.532);
	}
}
</style>