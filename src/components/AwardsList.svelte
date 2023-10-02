<script>
	import formatDate from '../utilities/formatDate';

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
		<div class="border border-gray-600 py-1.5 px-3 rounded">
			<h3 class="mb-1 text-xl">{award.awardName}</h3>
			<div class="flex gap-2 mb-0.5 text-gray-600 text-xs">
				<span>{formatDate(award.startDate)}</span>
				-
				<span>{formatDate(award.endDate)}</span>
			</div>
			<p class="text-sm text-gray-600">{award.description}</p>
		</div>
	{/each}
</div>
