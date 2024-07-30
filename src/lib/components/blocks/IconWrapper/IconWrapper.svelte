<script lang="ts">
	import { cn } from '$lib/utils.js';
	interface $$Props {
		class?: string | undefined;
	}
	let className: $$Props['class'] = undefined;
	export { className as class };
</script>

<div class={cn('h-fit w-fit rounded-sm bg-[#FF434D0D] p-2', className)}>
	<slot />
</div>
