<script>
	import { Container, Row, Col } from '@sveltestrap/sveltestrap';
	import NavMenu from '../components/NavMenu.svelte';
	import '../styles.css';
</script>

<Container fluid class="min-vh-100 vw-100 main-background-color mx-auto">
	<h1 class="text-white text-center mx-auto display-1 mb-4 fw-bold">ψέματα Technologies</h1>
	<Row class="d-flex flex-row mx-auto w-75 p-0 m-0 pb-5">
		<Col xxl={1} class="flex-shrink-1 me-sm-2 mb-2 p-0">
			<NavMenu />
		</Col>
		<Col class="border border-3 ms-0 w-100 overflow-scroll rounded secondary-background-color p-0">
			<slot />
		</Col>
	</Row>
</Container>
