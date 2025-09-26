<script>
    let { username } = $props()
</script>
<h1>Login</h1>
<div class="container">
    <img src="" alt="">
    <div class="form-container">
        <p>Bem-vindo de volta</p>
        <form>
            <input bind:value={username} type="text" name="username" id="username">
            <input type="text" name="senha">
            <button type="submit"><a href="./home">Login</a></button>
        </form>
    </div>
</div>

<style> 
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

</style>