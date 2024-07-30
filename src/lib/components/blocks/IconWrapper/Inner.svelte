<script lang="ts">
	import { cn } from '$lib/utils.js';
	interface $$Props {
		class?: string | undefined;
	}
	let className: $$Props['class'] = undefined;
	export { className as class };
</script>

<div class={cn('size-8 h-fit w-fit rounded-sm bg-white p-1 shadow-md', className)}>
	<slot />
</div>
