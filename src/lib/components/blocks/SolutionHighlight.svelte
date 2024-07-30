<script lang="ts">
	import Inner from '@/components/blocks/IconWrapper/Inner.svelte';
	import IconWrapper from '@/components/blocks/IconWrapper/IconWrapper.svelte';
	import TruckKun from '@/img/truck-kun.svelte';
	import { ArrowUpRight } from 'lucide-svelte';
</script>

<div
	class="mx-auto flex h-[40vh] w-[70vw] flex-col rounded-xl bg-gradient-to-l from-[#05A987] to-[#024336] text-center"
>
	<h3 class="mx-auto mt-16 text-4xl text-white">Unlock the Power of Our Solutions,</h3>
	<h3 class="mx-auto text-4xl text-white">Get FREE expert guidance.</h3>
	<button class="mx-auto mt-10 flex w-fit justify-between rounded-md bg-white p-3">
		Request Demo <ArrowUpRight /></button
	>
	<IconWrapper>
		<Inner>
			<TruckKun stroke="red" />
		</Inner>
	</IconWrapper>
</div>
