<script lang="ts">
	import { cn } from '$lib/utils.js';
	interface $$Props {
		mobile?: boolean | undefined;
		class?: string | undefined;
	}
	export let mobile = true;
	let className: $$Props['class'] = undefined;
	export { className as class };
</script>

<div class:lg:hidden={mobile} class:p-3={mobile} class="h-fit w-fit rounded-sm bg-[#FF434D0D] p-2">
	<div class={cn('size-8 h-fit w-fit rounded-sm bg-white p-1 shadow-md', className)}>
		<slot />
	</div>
</div>
