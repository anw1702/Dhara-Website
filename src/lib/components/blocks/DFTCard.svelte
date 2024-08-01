<script lang="ts">
</script>

<div
	class="flex flex-col justify-center gap-5 rounded-xl border border-solid border-black border-opacity-10 bg-white p-3.5 shadow-lg dark:bg-gray-800 md:w-fit md:max-w-[25vw] md:gap-3"
>
	<div
		class="flex h-10 w-10 items-center justify-center rounded-md bg-[#EBF5EB] px-2.5 py-2.5 dark:bg-gray-700"
	>
		<div class="aspect-square w-full">
			<slot name="icon" />
		</div>
	</div>
	<span class="mt-6 text-lg font-medium leading-6 text-zinc-800 dark:text-white">
		<slot name="heading"></slot>
	</span>
	<span class="mt-2 text-xs font-light leading-5 text-neutral-500 dark:text-gray-300">
		<slot name="body"></slot>
	</span>
</div>
