<script>
	import '../app.css';
	import Navbar from '@/components/blocks/navbar.svelte';
	import Footer from '@/components/blocks/footer.svelte';
	import { ModeWatcher } from 'mode-watcher';
</script>

<ModeWatcher />
<Navbar />
<div class="mt-20 md:mt-28">
	<slot></slot>
</div>
