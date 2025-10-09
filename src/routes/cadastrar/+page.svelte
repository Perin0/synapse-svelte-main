<script>
    let username = $state()
</script>
<h1>Cadastrar</h1>
<div class="container">
    <img src="https://img.freepik.com/premium-vector/e-learning-education-process-training-application-mobile-app-development-courses_566886-3834.jpg" alt="Imagem de cadastro">
    <div class="form-container">
        <p>Bem-vindo pela primeira vez</p>
        <form>
            <input bind:value={username} type="text" name="username" id="username">
            <input type="text" name="senha">
            <div class="radio-container">
                <input type="radio" name="op" id="ap" value="Qro Aprender">
                <label for="ap">Qro aprender</label>
                <input type="radio" name="op" id="en" value="Qro Ensinar">
                <label for="en">Qro ensinar</label>
            </div>
            <button type="submit"><a href="./home">Cadastrar</a></button>
        </form>
    </div>
</div>

<style>
    p{
        font-size: 1.25rem;
    }
    .radio-container{
        display: flex;
        flex-direction: row;
        width: 110%;
    }
    .container{
        display: flex;
        position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
        border: 1px solid black;
        padding: 2rem;
    }
    img{
        width: 500px;
        height: 500px;
        margin-left: auto;
        padding: 2rem;
    }
    form{
        display: flex;
        flex-direction: column;
        gap: 1rem;
    }
    .form-container{
        position: relative;
        top: 50%;
        transform: translateY(25%);
    }

</style>