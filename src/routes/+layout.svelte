<script>
	import '../app.postcss';
	import { AppShell } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/components/Navigation.svelte';
	import { initializeStores, Drawer } from '@skeletonlabs/skeleton';
	import Header from "$lib/components/Header.svelte";

	initializeStores();

</script>

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
		<h1>Hello</h1>
	</svelte:fragment>

</AppShell>
