<script>
	import formatDate from '../utilities/formatDate';
	export let award;
</script>

<div class="border border-gray-600 py-1.5 px-3 rounded">
	<h3 class="mb-1 text-xl">{award.awardName}</h3>
	<div class="flex gap-2 mb-0.5 text-gray-600 text-xs">
		<span>{formatDate(award.startDate)}</span>
		-
		<span>{formatDate(award.endDate)}</span>
	</div>
	<p class="text-sm text-gray-600">{award.description}</p>
</div>
