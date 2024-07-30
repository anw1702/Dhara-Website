<script lang="ts">
	import SolutionHighlight from '../lib/components/blocks/SolutionHighlight.svelte';
	import SupplyChainBreakthrough from '@/components/blocks/SupplyChainBreakthrough.svelte';
	import DFTFeaturesOverview from '@/components/blocks/DFTFeaturesOverview.svelte';
	import MainHeaderSection from '@/components/blocks/MainHeaderSection.svelte';
	import DftFeaturesCont from '@/components/blocks/DFTFeaturesCont.svelte';
	import Footer from '@/components/blocks/footer.svelte';
	import Scroller from '@/components/blocks/scroller.svelte';
	import Faq from '@/components/blocks/FAQ.svelte';
<<<<<<< HEAD
	import IntroDft from '@/components/blocks/IntroDFT.svelte';
=======
>>>>>>> f6150333d8f7018dc0bc0627575a6c73f8219705
</script>

<svelte:head>
	<title>Dhara | Revolutionizing Supply Chain Financing</title>
	<meta
		name="description"
		content="Explore Dhara's innovative solutions for supply chain financing, designed to empower businesses and streamline operations."
	/>
	<meta
		name="keywords"
		content="supply chain financing, Dhara, financial solutions, innovation, business growth"
	/>

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://dhara-website.netlify.app/" />
	<meta property="og:title" content="Dhara | Revolutionizing Supply Chain Financing" />
	<meta
		property="og:description"
		content="Explore Dhara's innovative solutions for supply chain financing, designed to empower businesses and streamline operations."
	/>
	<!-- Replace this later -->
	<meta property="og:image" content="URL_TO_IMAGE_ON_YOUR_SITE" />

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://dhara-website.netlify.app/" />
	<meta property="twitter:title" content="Dhara | Revolutionizing Supply Chain Financing" />
	<meta
		property="twitter:description"
		content="Explore Dhara's innovative solutions for supply chain financing, designed to empower businesses and streamline operations."
	/>
	<!-- Replace this later -->
	<meta property="twitter:image" content="URL_TO_IMAGE_ON_YOUR_SITE" />

	<!-- Structured Data -->
	<script type="application/ld+json">
		{
			"@context": "https://schema.org",
			"@type": "Organization",
			"url": "https://dhara-website.netlify.app/",
			"name": "Dhara",
			"logo": "URL_TO_LOGO",
			"description": "Dhara provides innovative solutions for supply chain financing, empowering businesses with efficient and effective financial strategies."
		}
	</script>
</svelte:head>

<MainHeaderSection />
<SupplyChainBreakthrough />
<<<<<<< HEAD
<IntroDft />
=======
>>>>>>> f6150333d8f7018dc0bc0627575a6c73f8219705
<DFTFeaturesOverview />
<SolutionHighlight />
<DftFeaturesCont />
<Faq />
<Footer />
<Scroller />
