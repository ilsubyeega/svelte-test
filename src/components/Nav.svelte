<script>
	export let segment;
</script>

<style>
	nav {
		font-weight: 300;
		padding: 0 1em;
		background: rgb(250, 250, 250);
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		height: 4px !important;
		margin-bottom: 0px !important;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
	a::after {
		border-radius: 100px;
		content: '';
		height: 0px;
		transition: all 0.15s;
		background-color: rgb(255,62,0);
		display: block;
		margin-top: 4px;
		margin-bottom: 4px;
	}
</style>

<nav>
	<ul>
		<li><a href='/' style="margin-right: 20px">ilsubyeega</a></li>
		<li><a class="item" aria-current='{segment === undefined ? "page" : undefined}' href='.'>home</a></li>
		<li><a class="item" aria-current='{segment === "about" ? "page" : undefined}' href='about'>about</a></li>
		<li><a class="item" href='https://discord.gg/WU4FjHk'>discord</a></li>

		<!-- for the blog link, we're using rel=prefetch so that Sapper prefetches
		     the blog data when we hover over the link or tap it on a touchscreen -->
		<!--<li><a rel=prefetch aria-current='{segment === "blog" ? "page" : undefined}' href='blog'>blog</a></li>-->
	</ul>
</nav>
