<script lang="ts">
</script>

<div
	class="mt-5 flex flex-col justify-center gap-5 rounded-xl border border-solid border-black border-opacity-10 bg-white p-3.5 shadow-lg"
>
	<div
		class="p-x-2.5 p-y-2.5 bg-fafa flex h-10 w-10 items-center justify-center rounded-md"
		style="background-color: #EBF5EB;"
	>
		<div class="aspect-square w-full">
			<slot name="icon" />
		</div>
	</div>
	<span class="mt-6 text-lg font-medium leading-6 text-zinc-800">
		<slot name="heading"></slot>
	</span>
	<span class="mt-2 text-xs font-light leading-5 text-neutral-500">
		<slot name="body"></slot>
	</span>
</div>
