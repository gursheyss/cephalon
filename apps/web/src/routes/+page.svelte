<script lang="ts">
	import { createQuery } from "@tanstack/svelte-query";
	import Input from "$lib/components/ui/input/input.svelte";
	import { orpc } from "$lib/orpc";

	const healthCheck = createQuery(orpc.healthCheck.queryOptions());

	import cephalon from "$lib/assets/cephalon.png";
</script>

<div class="min-h-screen flex flex-col items-center justify-center px-4">
	<div class="flex flex-col items-center space-y-6 w-full max-w-md">
		<img src={cephalon} alt="Cephalon" class="w-24 h-24 object-contain" />
		<div class="w-full">
			<Input />
		</div>
	</div>
</div>
