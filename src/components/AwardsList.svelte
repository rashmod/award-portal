<script>
	import Award from './Award.svelte';

	// to be changed to dynamic data
	const awards = new Array(10)
		.fill({
			id: Date.now(),
			awardName: 'Some prestigious award.',
			description:
				'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quibusdam, cupiditate. Lorem ipsum dolor sit amet consectetur adipisicing',
			startDate: Date.now(),
			endDate: Date.now(),
		})
		.map((item, i) => ({ ...item, id: item.id + i }));
</script>

<h1 class="mb-4 text-2xl font-bold text-center">Award lists</h1>
<div class="grid gap-4">
	{#each awards as award (award.id)}
		<Award {award} />
	{/each}
</div>
