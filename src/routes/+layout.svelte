<script>
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';
	import Navigation from '$lib/navigation/Navigation.svelte';
	import { initializeStores, Drawer, getDrawerStore } from '@skeletonlabs/skeleton';
	import { LightSwitch } from '@skeletonlabs/skeleton';

	initializeStores();

	const drawerStore = getDrawerStore();

	function drawerOpen() {
		drawerStore.open({});
	}
</script>

<Drawer>
	<Navigation />
</Drawer>

<!-- App Shell -->
<AppShell slotSidebarLeft="bg-surface-500/5 w-0 md:w-64">
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<div class="flex items-center">
					<button class="md:hidden btn btn-sm mr-4" on:click={drawerOpen}>
						<span>
							<svg viewBox="0 0 100 80" class="fill-token w-4 h-4">
								<rect width="100" height="20" />
								<rect y="30" width="100" height="20" />
								<rect y="60" width="100" height="20" />
							</svg>
						</span>
					</button>
					<a href="/">
						<strong class="text-base uppercase">Lukas Barragan Torres</strong>
					</a>
				</div>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<div class="hidden md:flex space-x-4">
					<a class="btn hover:variant-soft-primary" href="/skills">Skills</a>
					<a class="btn hover:variant-soft-primary" href="/resume">Resume</a>
					<a class="btn hover:variant-soft-primary" href="/portfolio">Portfolio</a>
					<a class="btn hover:variant-soft-primary" href="/contact">Contact</a>
				</div>
				<LightSwitch />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>

	<!-- Page Route Content -->
	<slot />
</AppShell>

