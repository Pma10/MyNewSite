<script>
    let nameReveal = false;
</script>

<div class="island" on:mouseenter={() => {nameReveal = true}} on:mouseleave={() => {nameReveal = false}}>
	{#if nameReveal}
	<img src="src\\routes\\profile.png" class="island-profile" alt="profile-img">
	<p class="island-title">프마</p>
	{/if}
</div>

<div>
	<ul class="nav-bar">
		<li><a href="/">Home</a></li>
		<li><a href="/about">About</a></li>
		<li><a href="/contact">Contact</a></li>
	</ul>
</div>

<div>
	<h1>Pma</h1>
	<h3>Developer</h3>
</div>

<style>
	@import url("https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable.min.css");
	:global(body){
		height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	a {
		text-decoration: none;
		color: black;
		transition: all 0.3s ease;
	}

	a:hover {
		letter-spacing: 0.2rem;
	}
	.nav-bar{
		position: fixed;
		left: 0;
		top: 45%;
		display: flex;
		flex-direction: column;
		font-family: 'Pretendard Variable';
		font-weight: 500;
	}
	.island {
		position: fixed;
		top: 1rem;
		width: 10rem;
		height: 3rem;
		border-radius: 2rem;
		background-color: black;
		transition: all 0.4s;
		color: #FFFFFF;
		display: flex;
		align-items: center;
		justify-content: flex-start;
		left: 50%;
		transform: translateX(-50%);
	}
	.island:hover {
		height: 6rem;
		width: 23rem;
	}
	.island-title {
		font-size: 2rem;
		margin-left: 1.5rem;
		font-family: 'Pretendard Variable';
		font-weight: 800;
	}
	.island-profile {
		width: 5rem;
		border-radius: 1rem;
		margin-left: 1rem;
	}
	@media (max-width: 768px) {
        .nav-bar {
            display: flex;
            flex-direction: row;
            top: 0;
            margin-top: 7.5rem;
        }
        .nav-bar li {
            margin: 0 1.6rem;
            list-style: none;
        }
    }
</style>

