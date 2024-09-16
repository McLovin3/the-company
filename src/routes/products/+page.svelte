<script lang="ts">
	import { Row, Col } from '@sveltestrap/sveltestrap';
	import { goto } from '$app/navigation';
	import keyboard from '$lib/images/keyboard.jpg';
	import mouse from '$lib/images/mouse.jpg';
	import prototype from '$lib/images/prototype.jpg';
</script>

<Row class="p-4 d-flex m-0">
	<Col class="m-0 p-0">
		<h2 class="text display-4 fw-bold">Our Products</h2>
		<p class="text">
			We offer top of the market, our products include top notch gaming mice, keyboards, and your
			personal companion “ prototype 667”. Prototype 667 can act as your friend, pet, and even
			family! It is authentic and is capable of singing, dancing, holding conversations, and even
			babysitting! If anything goes wrong with Prototype 667, be sure to use the implemented shock
			mechanism to fix him
		</p>

		<section class="text-center m-0">
			<h2 class="text display-4 fw-bold mt-5">Keyboards</h2>
			<p class="text">
				Our top of the market keyboards are made out of the most pristine materials available. They
				have interchangeable keys and have a crisp click with every button!
			</p>
			<img src={keyboard} class="rounded border border-3" alt="keyboard" />
			<div>
				<h2 class="text display-4 fw-bold mt-5">Mice</h2>
				<p class="text">
					Our mice are just as good as our keyboards! Made of top of the market materials, come with
					7 customizable side buttons, and they even come with a number pad of the other side!
				</p>
			</div>
			<img src={mouse} class="rounded border border-3" alt="mouse" />

			<div>
				<h2 class="text display-4 fw-bold mt-5">Prototype 667</h2>
				<p class="text">
					Prototype 667 is our top of the market ^̷à̵̷¢̶®̵ª̵†̷l̸x̷Q̶Ÿ̵U̵Ó̵̶ ̸í̵i̴Ş̶t̵Š̸›̷̸ö̸S̵̴å̵œ̴ ̵M̴Z̷³̶"̶Ó̷­̶ ̸^̷e̵Ï̶\̷]̸ô̷\̶}̷Ó̷!̴ş̸ä̶N̸ ̷¥̵,̷³̶$̷
					̶\̵[̷­̷Ò̴̴¾̶“̵Ğ̴Ô̴Ê̴„̶Ó̷Ş̷³̴­̷X̴ü̴²̶×̶n̴è̵̸v̸R̷ï̷§̶¯̶¼̶[̵ ̴“̸̴A̷™̴̶:̶6̶Š̶–̴M̴^̵à̷g̷¾̸é̵¹̵ó̸@̶¾̷g̵s̷̵ë̵š̸̶Ê̵R̶E̷(̶¼̷*̷2̷Š̵Ü̴̸…̴ ̸̵¯̶Ä̶õ̵̷^̶̵a̴@̷N̴å̴ ̵R̴ ̷‘̷b̵
					̴ƒ̷n̷í̴̴`̸0̵ã̷¼̷S̸Š̷̶î̶-̴Ú̴g̴4̵n̷,̶6̶Š̶–̴M̴
				</p>
			</div>
			<!-- svelte-ignore a11y-click-events-have-key-events -->
			<!-- svelte-ignore a11y-no-noninteractive-element-interactions -->
			<img
				src={prototype}
				on:click={() => goto('admin')}
				class="rounded border border-3"
				alt="prototype"
			/>
		</section>
	</Col>
</Row>

<style>
	@media (min-width: 768px) {
		img {
			width: 450px;
			height: 450px;
		}
	}

	@media (max-width: 768px) {
		img {
			width: 200px;
			height: 200px;
		}
	}
</style>
