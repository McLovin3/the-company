<script>
	import { Nav, NavItem, NavLink } from '@sveltestrap/sveltestrap';

	import { page } from '$app/stores';
	$page.url.pathname;

	const links = [
		{ name: 'Home', path: '/' },
		{ name: 'Hiring', path: '/hiring' },
		{ name: 'Our Products', path: '/products' }
	];
</script>

<Nav theme="dark">
	{#each links as link}
		<NavItem class="secondary-background-color rounded w-100 mb-2">
			<NavLink href={link.path}>
				<p class="p-0 m-0" class:active={$page.url.pathname === link.path}>
					{link.name}
				</p>
			</NavLink>
		</NavItem>
	{/each}
</Nav>

<style>
	p.active {
		color: #00adb5;
	}
</style>
