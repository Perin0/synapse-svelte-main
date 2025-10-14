<script>
    import { username } from '../../lib/svelte-stores';
</script>
<div class="aside">
    <div class="item">
        <img>
        <p>Dashboard</p>
    </div>
    <div class="item">
        <img>
        <p>Compromissoss</p>
    </div>
    <div class="item">
        <img>
        <p>Mensagens</p>
    </div>
    <div class="item">
        <img>
        <p>Revisões</p>
    </div>
    <div class="item">
        <img>
        <p>Configurações</p>
    </div>
</div>

<div class="center-container">
    <input type="text">
    <h1>bem vindo de volta {$username}</h1>
    Proximos compromisso
    <div class="compromissos">
        <img>
        <div class="comp-info-container">
            <p class="nome">Joao</p>
            <p class="date">Sexta, 19 de setembro</p>
        </div>
        <button>Ver detalhes</button>
    </div>
</div>

<style>
    .compromissos{
        display: flex;
        flex-direction: row;
        align-items: center;
        border: 1px solid black;
        padding: 1rem;
    }
    .center-container{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border: 1px solid black;
        padding: 5rem;
    }
    .aside{
        border: 1px solid black;
        width: fit-content;
        display: flex;
        flex-direction: column;
    }
    .item{
        margin: 1rem;
        border: 1px solid black;
        display: flex;
        flex-direction: row;
        align-items: center;
    }
    img{
        border: 1px solid black;
        width: 10px;
        height: 10px;
    }
</style>