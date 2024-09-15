<script>
	import { Container } from '@sveltestrap/sveltestrap';
	import NavMenu from '../components/NavMenu.svelte';
	import '../styles.css';
</script>

<Container fluid class="vh-100 main-background-color d-flex flex-column p-5">
	<h1 class="text-white mx-auto display-1 mb-4 fw-bold">ψέματα Technologies</h1>
	<div id="content" class="d-flex flex-row mx-auto">
		<div class="flex-shrink-1 me-2">
			<NavMenu />
		</div>
		<div class="border border-3 w-100 rounded secondary-background-color p-0 overflow-scroll">
			<slot />
		</div>
	</div>
</Container>

<style>
	#content {
		width: 90%;
		height: 80%;
	}
</style>
