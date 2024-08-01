<script lang="ts">
	import { TelInput, normalizedCountries } from 'svelte-tel-input';
	import type { DetailedValue, CountryCode, E164Number } from 'svelte-tel-input/types';

	// Any Country Code Alpha-2 (ISO 3166)
	let country: CountryCode | null = 'IN';

	// You must use E164 number format. It's guarantee the parsing and storing consistency.
	let value: E164Number | null = '+91 98765 43210';

	// Validity
	let valid = true;

	// Optional - Extended details about the parsed phone number
	let detailedValue: DetailedValue | null = null;
</script>

<div class="wrapper">
	<select
		class="h-[36px] rounded-md border border-solid pl-3 pr-3 outline-none {!valid
			? 'border-red-700'
			: ''}"
		aria-label="Default select example"
		name="Country"
		bind:value={country}
	>
		<option value={null} hidden={country !== null}>Please select</option>
		{#each normalizedCountries as currentCountry (currentCountry.id)}
			<option
				value={currentCountry.iso2}
				selected={currentCountry.iso2 === country}
				aria-selected={currentCountry.iso2 === country}
			>
				{currentCountry.iso2} (+{currentCountry.dialCode})
			</option>
		{/each}
	</select>
	<label for="phoneNumber" class="sr-only">Phone Number</label>
	<TelInput
		name="phoneNumber"
		required
		bind:country
		bind:value
		bind:valid
		bind:detailedValue
		class="h-[32px] rounded-md pl-3 pr-3 outline-none {!valid ? 'border-red-700' : ''}"
	/>
</div>
