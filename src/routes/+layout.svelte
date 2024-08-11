<script>
	import '../app.postcss';
	import { AppShell } from '@skeletonlabs/skeleton';
	import Navigation from './Navigation.svelte';
	import { initializeStores, Drawer, Modal } from '@skeletonlabs/skeleton';
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import StarLegendModal from "./skills/StarLegendModal.svelte";
	import { afterNavigate } from '$app/navigation';

	const modalRegistry = {
		// Set a unique modal ID, then pass the component reference
		modalComponentOne: { ref: StarLegendModal },
		// ...
	};

	// Fix scroll issue bug: https://github.com/sveltejs/kit/issues/2733
	afterNavigate(() => {
		document.getElementById('page')?.scrollTo(0, 0);
	});


	initializeStores();

</script>

<Modal components={modalRegistry} />

<Drawer>
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-0 md:w-64" slotFooter="bg-black p-4">
	<svelte:fragment slot="header">
		<Header/>
	</svelte:fragment>

	<!-- Page Content -->
	<slot />

	<!-- Page Footer -->
	<svelte:fragment slot="pageFooter">
		<Footer/>
	</svelte:fragment>

</AppShell>
