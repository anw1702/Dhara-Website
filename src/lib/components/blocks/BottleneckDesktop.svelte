<script lang="ts">
	export let border: string = '';
	export let iconColor: string = '';
</script>

<div
	class="flex h-full min-h-[45vh] flex-col rounded-3xl border-b-[20px] transition-colors {border} bg-white p-4 drop-shadow-md dark:bg-gray-800"
>
	<div
		class="mb-16 mt-3 size-fit rounded-lg {iconColor} p-2 dark:border-transparent dark:bg-gray-700"
	>
		<slot name="icon" />
	</div>
	<div class="my-5 text-xl dark:text-white">
		<slot name="heading" />
	</div>
	<div class="text-base text-gray-500 dark:text-gray-400">
		<slot name="body" />
	</div>
</div>
