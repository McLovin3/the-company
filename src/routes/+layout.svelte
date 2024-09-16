<script>
	import { Container, Row, Col } from '@sveltestrap/sveltestrap';
	import NavMenu from '../components/NavMenu.svelte';
	import '../styles.css';
</script>

<Container fluid class="min-vh-100 min-vw-100 main-background-color d-flex flex-column p-5">
	<h1 class="text-white text-center mx-auto display-1 mb-4 fw-bold">ψέματα Technologies</h1>
	<div id="content" class="d-flex flex-row mx-auto">
		<Row>
			<Col xxl={1} class="flex-shrink-1 me-sm-2">
				<NavMenu />
			</Col>
			<Col class="border border-3 w-100 rounded secondary-background-color p-0 overflow-scroll">
				<slot />
			</Col>
		</Row>
	</div>
</Container>

<style>
	#content {
		width: 90%;
		height: 80%;
	}
</style>
