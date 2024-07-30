<script lang="ts">
	import Inner from '@/components/blocks/IconWrapper/Inner.svelte';
	import IconWrapper from '@/components/blocks/IconWrapper/IconWrapper.svelte';
	import TruckKun from '@/img/truck-kun.svelte';
	import Cart from '@/img/cart.svelte';
	import Shop from '@/img/shop.svelte';
	import Building from '@/img/building.svelte';
	import { ArrowUpRight } from 'lucide-svelte';
</script>

<div
	class="relative mx-auto mt-12 mb-12 flex h-[40vh] w-[70vw] flex-col rounded-xl bg-gradient-to-l from-[#05A987] to-[#024336] text-center"
>
	<h3 class="mx-auto mt-16 text-4xl text-white">Unlock the Power of Our Solutions,</h3>
	<h3 class="mx-auto text-4xl text-white">Get FREE expert guidance.</h3>
	<button class="mx-auto mt-10 flex w-fit justify-between rounded-md bg-white p-3">
		Request Demo <ArrowUpRight /></button
	>
	<!-- Added Icons inside the main box -->
	<div class="absolute top-0 left-0 mt-[50px] ml-[50px]">
		<IconWrapper class="bg-[#035D4A] p-[5px] rounded-[10px]">
			<Inner class="bg-[#05A987] rounded-[5px]">
				<Building stroke="White"/>
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute top-0 right-0 mt-[50px] mr-[50px]">
		<IconWrapper class="bg-[#035D4A] p-[5px] rounded-[10px]">
			<Inner class="bg-[#05A987] rounded-[5px]">
				<TruckKun stroke="White"/>
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute bottom-0 left-0 mb-[50px] ml-[200px]">
		<IconWrapper class="bg-[#035D4A] p-[5px] rounded-[10px]">
			<Inner class="bg-[#05A987] rounded-[5px]">
				<Shop stroke="White"/>
			</Inner>
		</IconWrapper>
	</div>
	<div class="absolute bottom-0 right-0 mb-[50px] mr-[200px]">
		<IconWrapper class="bg-[#035D4A] p-[5px] rounded-[10px]">
			<Inner class="bg-[#05A987] rounded-[5px]">
				<Cart stroke="White"/>
			</Inner>
		</IconWrapper>
	</div>
</div>
