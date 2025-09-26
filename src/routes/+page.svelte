<div class="left-aligned">
	<button><a href="./cadastrar">Qro aprender</a></button>
	<button><a href="./cadastrar">Qro ensinar</a></button>
	<button><a href="./login">Login</a></button>
</div>
<div class="center-text">
	<h1>Conectando pessoas que querem aprender com mentores que querem ensinar</h1>
	<h2>Encontre mentores experientes para aprender de forma rápida e personalizada</h2>
	<input placeholder="Pesquisar" />
</div>
<div class="mentors-div">
	<p>Mentores em destaque</p>
	<div class="mentors-card-container">
		<div class="card"></div>
		<div class="card"></div>
		<div class="card"></div>
	</div>
</div>

<style>
	.left-aligned {
		position: absolute;
		max-width: fit-content;
		margin-left: auto;
	}
	.center-text {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		gap: 1rem;
	}
	.mentors-div {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}
	.mentors-card-container {
		display: flex;
		flex-direction: row;
	}
	.card {
		width: 100px;
		height: 100px;
		border: 1px solid black;
	}
</style>
