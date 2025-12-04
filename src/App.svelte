<script>
	import { getEventLogLocation , parseEvents, createCitation } from './eventlog';

	let location;
    let claims = [];

	loadEventLog();

	async function loadEventLog() {
		location = await getEventLogLocation();
		claims = await parseEvents(location);
	}	
</script>

<main>
 {#each claims as claim}
 	<div class="claim-item">
		{@html createCitation(claim)}	
	</div>
 {/each}
</main>