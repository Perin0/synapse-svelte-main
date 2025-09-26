
<nav class="navbar">
	<h1 class="logo">Logo</h1>
	<slot name="btns"></slot>
</nav>
<main>
	<slot/>
</main>

<style>
	.navbar {
		display: flex;
		flex-direction: row;
	}
</style>
