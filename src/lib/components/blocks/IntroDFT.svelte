<script lang="ts">
	import DFTFeature from './IntroDFTFeature.svelte';
	import BackgroundLines from './BackgroundLines.svelte';
	import clock from '@/img/clock.svg';
	import searchtick from '@/img/searchtick.svg';
	import securetick from '@/img/securetick.svg';


	interface Feature {
		icon: string;
		title: string;
		description: string;
	}

	const features: Feature[] = [
		{
			icon: [clock],
			title: 'Immediacy',
			description:
				'Transactions with DFTs are processed swiftly, a stark contrast to the often-protracted procedures of conventional financing!'
		},
		{
			icon: [searchtick],
			title: 'Transparency',
			description:
				'Each transaction is recorded on a blockchain, offering an undisputable and clear record of transactions, accessible to all relevant parties!'
		},
		{
			icon: [securetick],
			title: 'Security',
			description:
				'Leveraging the robustness of blockchain technology, DFTs provide a secure environment for financial transactions, safeguarding against tampering and fraud.'
		}
	];
</script>

<section class="flex flex-col justify-center pt-20">
	<section
		class="relative flex w-full flex-shrink-0 flex-col items-center justify-center bg-gradient-to-l from-[#05A987] to-[#024336] to-85% px-16 py-20 max-lg:max-w-full max-lg:px-5"
	>
		<BackgroundLines />
		<div class="relative w-full max-w-screen-xl max-lg:max-w-full">
			<div class="flex gap-5 max-lg:flex-col">
				<div class="flex w-[45%] flex-col max-lg:ml-0 max-lg:w-full">
					<div class="relative grow max-lg:mt-10 max-lg:max-w-full">
						<div class="flex gap-6 max-lg:flex-col">
							<div class="flex w-6/12 flex-col max-lg:ml-0 max-lg:w-full">
								<div class="relative flex grow flex-col text-white max-lg:mt-5">
									<DFTFeature feature={features[0]} />
									<DFTFeature feature={features[1]} />
								</div>
							</div>
							<div class="ml-5 flex w-6/12 flex-col text-white max-lg:ml-0 max-lg:w-full">
								<DFTFeature feature={features[2]} />
							</div>
						</div>
					</div>
				</div>
				<div class="ml-5 flex w-[50%] flex-col px-20 max-lg:ml-0 max-lg:w-full">
					<div
						class="relative my-auto flex flex-col self-stretch text-white max-lg:mt-10 max-lg:max-w-full"
					>
						<h2
							class="text-6xl font-medium leading-[66px] max-lg:max-w-full max-lg:text-4xl max-lg:leading-[49px]"
						>
							Introducing DFT <br />Tokens
						</h2>
						<p class="mt-5 text-xl font-light leading-8 tracking-wide max-lg:max-w-full">
							DFTs represent a paradigm shift in supply chain finance, offering a digital,
							blockchain-based approach to managing and transferring value within the supply chain
							ecosystem.
						</p>
					</div>
				</div>
			</div>
		</div>
	</section>
</section>


