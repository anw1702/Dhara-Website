<script lang="ts">
	export let border: string = '';
	export let iconColor: string = 'EBF5EB';
</script>

<div
	class="mb-5 flex flex-col rounded-2xl border-b-[20px] {border} bg-white p-4 drop-shadow-lg dark:bg-gray-800"
>
	<div
		class="mb-6 mt-3 size-fit rounded-lg {iconColor} p-2 dark:border-transparent dark:bg-gray-700"
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
