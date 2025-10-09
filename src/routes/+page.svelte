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
		<div class="card"><button class="see-profile">Ver perfil</button></div>
		<div class="card"><button class="see-profile">Ver perfil</button></div>
		<div class="card"><button class="see-profile">Ver perfil</button></div>
	</div>
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap');
	
	h2{
		font-weight: 400;
		margin-top: 0;
	}
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
		input{
			background: url("https://static.thenounproject.com/png/101791-200.png") no-repeat left;
			background-size: 1.5rem;
			width: 300px;
			height: 40px;
			border-radius: 8px;
			border: 1px solid #ccc;
			padding: 0 10px 0px 30px;
			font-size: 16px;
			box-shadow: 0px 0px 20px 3px rgba(0, 0, 0, 0.1);
		}
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
		gap: 1rem
	}
	.card {
		background: url(https://avatarfiles.alphacoders.com/371/thumb-1920-371486.png) no-repeat center;
		background-size: 125px 125px;
		position: relative;
		width: 150px;
		height: 150px;
		border: 1px solid black;
		border-radius: 5px;
	}
	.see-profile {
		position: absolute;
		bottom: 10px;
		left: 50%;
		transform: translateX(-50%);
		border-radius: 15px;
		background-color: #0088ff;
		color: white;
		padding: 5px;
	}
</style>
