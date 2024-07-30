<script lang="ts">
	import Inner from '@/components/blocks/IconWrapper/Inner.svelte';
	import IconWrapper from '@/components/blocks/IconWrapper/IconWrapper.svelte';
	import TruckKun from '@/img/truck-kun.svelte';
	import Cart from '@/img/cart.svelte';
	import Shop from '@/img/shop.svelte';
	import Building from '@/img/building.svelte';
	import { ArrowUpRight } from 'lucide-svelte';
	import UnlockLeft from '@/img/UnlockLeft.svelte';
	import UnlockRight from '@/img/UnlockRight.svelte';
</script>

<div
	class="relative mx-auto mb-12 mt-12 flex h-[40vh] w-[70vw] flex-col rounded-xl bg-gradient-to-l from-[#05A987] to-[#024336] text-center"
>
	<span class="absolute">
		<UnlockRight />
	</span>
	<h3 class="mx-auto mt-16 text-4xl text-white">Unlock the Power of Our Solutions,</h3>
	<h3 class="mx-auto text-4xl text-white">Get FREE expert guidance.</h3>
	<button class="mx-auto mt-10 flex w-fit justify-between rounded-md bg-white p-3">
		Request Demo <ArrowUpRight /></button
	>
	<!-- Added Icons inside the main box -->
	<div class="absolute left-0 top-0 ml-[50px] mt-[50px]">
		<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px]">
			<Inner class="rounded-[5px] bg-[#05A987]">
				<Building stroke="white" />
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute right-0 top-0 mr-[50px] mt-[50px]">
		<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px]">
			<Inner class="rounded-[5px] bg-[#05A987]">
				<TruckKun stroke="white" />
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute bottom-0 left-0 mb-[50px] ml-[200px]">
		<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px]">
			<Inner class="rounded-[5px] bg-[#05A987]">
				<Shop stroke="white" />
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute bottom-0 right-0 mb-[50px] mr-[200px]">
		<IconWrapper class="rounded-[10px] bg-[#035D4A] p-[5px]">
			<Inner class="rounded-[5px] bg-[#05A987]">
				<Cart stroke="white" />
			</Inner>
		</IconWrapper>
	</div>
	<span class="absolute right-0">
		<UnlockLeft />
	</span>
</div>
