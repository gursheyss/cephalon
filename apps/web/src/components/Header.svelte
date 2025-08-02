<script lang="ts">
	import cephalon from "$lib/assets/cephalon.png";
	import cy from "$lib/assets/cy.png";
	import jordas from "$lib/assets/jordas.png";
	import ordis from "$lib/assets/ordis.png";
	import simaris from "$lib/assets/simaris.png";
	import suda from "$lib/assets/suda.png";
	import UserMenu from "./UserMenu.svelte";

	const otherAssets = [
		{ src: jordas, alt: "Jordas" },
		{ src: suda, alt: "Suda" },
		{ src: ordis, alt: "Ordis" },
		{ src: simaris, alt: "Simaris" },
		{ src: cy, alt: "Cy" },
	];
</script>

<div class="container mx-auto px-4 py-2 md:px-6">
	<div class="flex flex-row items-center justify-between">
		<!-- Left side: Cephalon logo -->
		<div class="flex items-center">
			<img
				src={cephalon}
				alt="Cephalon"
				class="w-32 h-8 object-contain pixel-art dark:invert"
			/>
		</div>

		<!-- Right side: Other assets and user menu -->
		<div class="flex items-center">
			{#each otherAssets as asset (asset.alt)}
				<img
					src={asset.src}
					alt={asset.alt}
					class="w-8 h-8 object-contain pixel-art"
				/>
			{/each}
			<UserMenu />
		</div>
	</div>
</div>

<style>
	.pixel-art {
		image-rendering: pixelated;
		image-rendering: -moz-crisp-edges;
		image-rendering: crisp-edges;
	}
</style>
