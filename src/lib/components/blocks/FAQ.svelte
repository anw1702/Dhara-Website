<script lang="ts">
	import { ChevronDown } from 'lucide-svelte';
	import * as Accordion from '$lib/components/ui/accordion';

	let faqs = [
		{
			question: 'How does DFT integrate with existing financial systems?',
			answer:
				'DFT is designed for easy integration with traditional financial systems and digital payment platforms, ensuring a seamless transition to blockchain-based finance.'
		},
		{
			question: 'Is DFT suitable for businesses of all sizes?',
			answer:
				'Yes, DFT is designed to cater to businesses of all sizes, providing scalable solutions tailored to their specific needs.'
		},
		{
			question: 'What makes DFT more secure than traditional finance methods?',
			answer:
				'DFT leverages blockchain technology to enhance security, offering encrypted transactions and decentralized validation to prevent fraud and ensure data integrity.'
		},
		{
			question: 'Is DFT scalable for businesses with varying volumes of receivables?',
			answer:
				"Absolutely, DFT's flexible architecture allows businesses to manage varying volumes of receivables efficiently, scaling up or down based on their requirements."
		}
	];
</script>

<div class="overflow-hidden px-20 py-10 max-md:px-5">
	<div class="flex gap-5 max-md:flex-col">
		<div class="flex w-[36%] flex-col max-md:ml-0 max-md:w-full">
			<div class="my-auto flex flex-col self-stretch max-md:mt-10 max-md:max-w-full">
				<div
					class="text-4xl font-medium leading-10 text-zinc-800 dark:text-white max-md:max-w-full"
				>
					Frequently Asked <br />Questions
				</div>
				<div class="mt-5 text-lg font-light leading-7 text-neutral-500 max-md:max-w-full">
					Here is the list of FAQ’s about us and how we work. Got more questions? Feel free to reach
					us out
				</div>
			</div>
		</div>
		<div class="ml-5 flex w-[64%] flex-col max-md:ml-0 max-md:w-full">
			<div class="grow max-md:mt-10 max-md:max-w-full">
				{#each faqs as { question, answer }, index}
					<div class="mb-4">
						<Accordion.Root class="group rounded-md border border-gray-200">
							<Accordion.Item value="item-{index}">
								<Accordion.Trigger
									class="flex cursor-pointer justify-between rounded-md bg-white px-4 py-2 text-left dark:bg-black"
									>{question}</Accordion.Trigger
								>
								<Accordion.Content class="mt-2 bg-white p-4 dark:bg-black">
									{answer}
								</Accordion.Content>
							</Accordion.Item>
						</Accordion.Root>
					</div>
				{/each}
			</div>
		</div>
	</div>
</div>
