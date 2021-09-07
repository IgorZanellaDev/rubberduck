<script>
	import 'carbon-components-svelte/css/g100.css';
	import { Header, HeaderNav, HeaderNavItem } from 'carbon-components-svelte';
</script>

<Header platformName="RubberDuck" href="/">
	<HeaderNav style="display: block !important">
		<HeaderNavItem href="#what-is-rubber-duck" text="What is Rubber Duck?" />
	</HeaderNav>
</Header>

<slot></slot>