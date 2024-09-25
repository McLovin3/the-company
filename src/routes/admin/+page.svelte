<script lang="ts">
	import { Button, FormGroup, Input, Label, Form } from '@sveltestrap/sveltestrap';

	let loggedIn = false;
	let incorrectPassword = false;
	let password = '';
	let shake = false;

	function onSubmit() {
		if (password === 'Admin-DontLetThemOut') {
			loggedIn = true;
		} else {
			incorrectPassword = true;
			shake = true;
			setTimeout(() => {
				shake = false;
			}, 500);
		}
	}
</script>

<div class="d-flex">
	<Form on:submit={onSubmit} class="w-75 mx-auto align-self-center text-center">
		<FormGroup>
			{#if loggedIn}
				<h3 class="text-white fw-bold">
					Congratulations! You have cracked the code…. More coming soon!
				</h3>
			{:else}
				<Label class="display-5 text-white fw-bold">Admin Login</Label>
				<Input
					autocomplete="off"
					bind:value={password}
					required
					placeholder="Enter password"
					class="mb-3"
					type="password"
				/>
				{#if incorrectPassword}
					<p class:animated={shake} class="text-danger fw-bold horizontal-shaking">Access Denied</p>
				{/if}
				<Button type="submit" class="border border-3 text-dark fw-bold">Login</Button>
			{/if}
		</FormGroup>
	</Form>
</div>

<style>
	.animated {
		animation: horizontal-shaking 0.5s normal;
	}

	@keyframes horizontal-shaking {
		0% {
			transform: translateX(0);
		}
		33% {
			transform: translateX(-5px);
		}
		66% {
			transform: translateX(5px);
		}
		100% {
			transform: translateX(0);
		}
	}

	div {
		min-height: 400px;
	}
</style>
