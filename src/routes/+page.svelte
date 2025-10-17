<script lang="ts">
	import MentorCard from "$lib/components/MentorCard.svelte";

	type Mentor = {
		id: number;
		name: string;
		specialty: string;
		avatarUrl: string;
		rating: number;
		reviewCount: number;
		price: number;
	};
	const featuredMentors: Mentor[] = [
		{
			id: 1,
			name: 'Carla Pereira',
			specialty: 'Inglês',
			avatarUrl: 'https://i.pravatar.cc/150?img=1', // Usando avatares de placeholder
			rating: 5,
			reviewCount: 43,
			price: 30.0
		},
		{
			id: 2,
			name: 'João Silva',
			specialty: 'Programação',
			avatarUrl: 'https://i.pravatar.cc/150?img=3',
			rating: 5,
			reviewCount: 200,
			price: 40.0
		},
		{
			id: 3,
			name: 'Lucas Souza',
			specialty: 'Matemática',
			avatarUrl: 'https://i.pravatar.cc/150?img=5',
			rating: 5,
			reviewCount: 188,
			price: 35.0
		}
	];
</script>

<div class="page-container">
	<header class="main-header">
		<a href="/" class="logo">MentorOn</a>
		<nav class="nav-links">
			<a href="/learn" class="btn btn-secondary">Quero Aprender</a>
			<a href="/login" class="btn btn-primary">Login</a>
		</nav>
	</header>

	<main>
		<section class="hero-section">
			<h1>Conectando pessoas que querem aprender com mentores que ensinam</h1>
			<p class="subtitle">Encontre mentores experientes para aprender de forma rápida e personalizada</p>
			
			<div class="search-bar">
				<div class="search-input-wrapper">
					<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>
					<input type="search" placeholder="Buscar por habilidade" />
				</div>
				<button class="filter-dropdown">
					Todos
					<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="6 9 12 15 18 9"></polyline></svg>
				</button>
			</div>
		</section>

		<section class="mentors-section">
			<h2>Mentores em destaque</h2>
			
			<div class="mentors-grid">
				{#each featuredMentors as mentor (mentor.id)}
					<MentorCard mentor={mentor}/>
				{/each}
			</div>
		</section>
	</main>
</div>

<style>
	/* Definição de variáveis de estilo para fácil customização */
	:root {
		--primary-blue: #007aff;
		--light-gray-bg: #f7f7f7;
		--card-border-color: #e0e0e0;
		--text-dark: #1a1a1a;
		--text-light: #555;
		--star-color: #ffc700;
		--font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
	}

	/* Estilos Globais e do Container Principal */
	.page-container {
		font-family: var(--font-family);
		background-color: #fff;
		max-width: 1200px;
		margin: 0 auto;
		padding: 0 2rem;
	}

	/* Estilos do Cabeçalho */
	.main-header {
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding: 1.5rem 0;
	}

	.logo {
		font-size: 1.75rem;
		font-weight: 700;
		color: var(--text-dark);
		text-decoration: none;
	}

	.nav-links {
		display: flex;
		align-items: center;
		gap: 1rem;
	}
	
	/* Estilos dos Botões */
	.btn {
		padding: 0.75rem 1.5rem;
		border-radius: 8px;
		border: none;
		font-weight: 600;
		font-size: 1rem;
		cursor: pointer;
		text-decoration: none;
		display: inline-block;
		text-align: center;
		transition: transform 0.2s ease;
	}

	.btn:hover {
		transform: translateY(-2px);
	}

	.btn-primary {
		background-color: var(--primary-blue);
		color: white;
	}
    
    .btn-secondary {
        background-color: transparent;
        color: var(--text-dark);
    }
	/* Estilos da Seção Hero */
	.hero-section {
		text-align: center;
		padding: 4rem 0;
        background-color: var(--light-gray-bg);
        border-radius: 16px;
        margin-top: 2rem;
	}

	.hero-section h1 {
		font-size: 3rem;
		font-weight: 700;
		color: var(--text-dark);
		max-width: 700px;
		margin: 0 auto 1rem;
	}

	.hero-section .subtitle {
		font-size: 1.25rem;
		color: var(--text-light);
		margin-bottom: 2.5rem;
	}
    
    /* Barra de Busca */
    .search-bar {
        display: flex;
        justify-content: center;
        gap: 1rem;
        max-width: 600px;
        margin: 0 auto;
    }

    .search-input-wrapper {
        position: relative;
        flex-grow: 1;
    }

    .search-input-wrapper svg {
        position: absolute;
        left: 1rem;
        top: 50%;
        transform: translateY(-50%);
        color: var(--text-light);
    }

    .search-input-wrapper input {
        width: 100%;
        padding: 1rem 1rem 1rem 3rem;
        border: 1px solid var(--card-border-color);
        border-radius: 8px;
        font-size: 1rem;
        background-color: white;
    }

    .filter-dropdown {
        display: flex;
        align-items: center;
        gap: 0.5rem;
        padding: 1rem;
        border: 1px solid var(--card-border-color);
        border-radius: 8px;
        background-color: white;
        font-size: 1rem;
        cursor: pointer;
    }

	/* Estilos da Seção de Mentores */
	.mentors-section {
		padding: 5rem 0;
	}

	.mentors-section h2 {
		font-size: 2.25rem;
		font-weight: 700;
		margin-bottom: 2.5rem;
		color: var(--text-dark);
	}

	.mentors-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
		gap: 2rem;
	}

    /* Media queries para responsividade */
    @media (max-width: 768px) {
        .hero-section h1 {
            font-size: 2.25rem;
        }
        .nav-links .btn-secondary {
            display: none; /* Esconde o botão "Quero Aprender" em telas pequenas */
        }
        .search-bar {
            flex-direction: column;
        }
    }
</style>