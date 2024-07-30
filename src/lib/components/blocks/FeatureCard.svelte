<script lang="ts">
	export let color = '';
</script>

<div class="flex items-center space-x-4 rounded-md bg-white p-4 drop-shadow-lg dark:bg-gray-800">
	<div class="rounded-lg {color} p-2 text-white">
		<slot name="icon" />
	</div>
	<span>
		<slot />
	</span>
</div>
