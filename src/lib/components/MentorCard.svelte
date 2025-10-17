<script lang="ts">
	type Mentor = {
		name: string;
		specialty: string;
		avatarUrl: string;
		reviewCount: number;
		price: number;
	};

	export let mentor: Mentor;
</script>

<article class="mentor-card">
	<div class="mentor-info">
		<img src={mentor.avatarUrl} alt="Avatar de {mentor.name}" class="mentor-avatar" />
		<div class="mentor-details">
			<h3>{mentor.name}</h3>
			<p class="mentor-specialty">{mentor.specialty}</p>
		</div>
	</div>
	<div class="mentor-rating">
		<span>★★★★★</span>
		<span class="review-count">({mentor.reviewCount})</span>
	</div>
	<p class="mentor-price">R${mentor.price.toFixed(2).replace('.', ',')}</p>
	<button class="btn btn-primary full-width">Ver perfil</button>
</article>

<style>
	.mentor-card {
		background-color: #f7f7f7;
		border: 1px solid #e0e0e0;
		border-radius: 16px;
		padding: 1.5rem;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
	/* ... e todos os outros estilos relacionados ao card (.mentor-info, .mentor-avatar, etc.) */
	/* Adicione o restante dos estilos do card aqui */
    .mentor-info { display: flex; align-items: center; gap: 1rem; }
    .mentor-avatar { width: 60px; height: 60px; border-radius: 50%; object-fit: cover; }
    .mentor-details h3 { margin: 0; font-size: 1.25rem; font-weight: 600; color: #1a1a1a; }
    .mentor-specialty { margin: 0; color: #555; }
    .mentor-rating { color: #555; }
    .mentor-rating span:first-child { color: #ffc700; letter-spacing: 2px; }
    .mentor-price { font-size: 1.75rem; font-weight: 700; color: #1a1a1a; margin: 0; }
    /* Os estilos dos botões podem ser movidos para um local global ou para o componente Button depois */
    .btn { padding: 0.75rem 1.5rem; border-radius: 8px; border: none; font-weight: 600; font-size: 1rem; cursor: pointer; text-decoration: none; display: inline-block; text-align: center; transition: transform 0.2s ease; }
    .btn:hover { transform: translateY(-2px); }
    .btn-primary { background-color: #007aff; color: white; }
    .full-width { width: 100%; }
</style>