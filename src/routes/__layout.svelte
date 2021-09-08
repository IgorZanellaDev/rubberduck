<script>
	import 'carbon-components-svelte/css/g100.css';
	import { Column, Grid, Header, HeaderNav, HeaderNavItem, Link, Row } from 'carbon-components-svelte';
</script>

<Header platformName="RubberDuck" href="/">
	<HeaderNav style="display: block !important">
		<HeaderNavItem href="#what-is-rubber-duck" text="What is Rubber Duck?" />
	</HeaderNav>
</Header>

<slot></slot>

<Grid>
	<Row>
		<Column class="footer-column" style="text-align: center; display: flex; justify-content: center; align-items: center; height: 36px">
			<div>
				Made with <span style="color: #e25555;">&#9829;</span> by <Link href="https://igorzanella.dev" target="_blank" rel="noopener">igorzanella.dev</Link>
			</div>
		</Column>
	</Row>
</Grid>