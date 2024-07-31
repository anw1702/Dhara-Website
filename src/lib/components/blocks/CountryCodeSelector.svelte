<script lang="ts">
	let countries = [
		{ code: '+91', name: 'India', flag: '🇮🇳' },
		{ code: '+1', name: 'United States', flag: '🇺🇸' },
		{ code: '+44', name: 'United Kingdom', flag: '🇬🇧' },
		// Add more countries as needed
	];
	let selectedCountry: { code: string; name: string; flag: string } = countries[0];

	function handleCountryChange(event: Event) {
		const target = event.target as HTMLSelectElement;
		const countryCode = target.value;
		selectedCountry = countries.find(country => country.code === countryCode) || countries[0];
	}
</script>

<div class="relative w-22">
	<select 
		on:change={handleCountryChange} 
		class="appearance-none w-full py-2 pl-3 pr-8 bg-white border border-gray-300 rounded leading-tight focus:outline-none focus:border-gray-500"
	>
		{#each countries as country}
			<option value={country.code}>
				<span class=" w-6 h-6 rounded-full border border-gray-300 mr-2 flex items-center justify-center text-xl">
					{country.flag}
				</span>
				{country.code}
			</option>
		{/each}
	</select>
	<div class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700">
		<svg class="fill-current h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"><path d="M7 10l5 5 5-5H7z"/></svg>
	</div>
</div>

<style>
	select {
		-webkit-appearance: none;
		-moz-appearance: none;
		appearance: none;
	}

	span {
		font-size: 1.5rem; /* Adjust the size of the emoji */
	}
</style>
