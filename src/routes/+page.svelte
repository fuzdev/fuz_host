<script lang="ts">
	import { resolve } from '$app/paths';
</script>

<main class="width_atmost_sm px_lg pb_xl9">
	<section class="box">
		<h1 class="mt_xl2">fuz_host</h1>
		<p>host APIs for JS: filesystem, processes, and the OS, one import across runtimes</p>
		<p>
			Experimental, with no API yet. It will be published as <code>@fuzdev/fuz_host</code>.
		</p>
		<p>
			<a href={resolve('/about')}>about</a> · <a href={resolve('/docs')}>docs</a> ·
			<a href="https://github.com/fuzdev/fuz_host">source</a>
		</p>
	</section>
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: 0 auto;
	}
</style>
