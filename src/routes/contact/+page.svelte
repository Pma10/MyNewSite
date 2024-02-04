
<script>
    let nameReveal = false;

</script>

<div class="island" on:mouseenter={() => {nameReveal = true}} on:mouseleave={() => {nameReveal = false}}>
	{#if nameReveal}
	<img src="src\lib\images\profile.png" class="island-profile" alt="profile-img">
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

<div class="index-content">
	<h1 >저에게 연락 가능한 연락처에요!</h1>
	<h2><a href="https://discord.com/users/959696962523914260" target="_blank"><img src="src\lib\images\discord.png" width="60px" class="contact-img"></a></h2>
</div>

<style>
	@import url("https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable.min.css");
	:global(body){
		height: 100vh;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.contact-img{
		border-radius: 1rem;
		display: flex;
		margin: 0 auto;
		transition: all 0.3s ease;
	}
	.contact-img:hover{
		transform: scale(1.3);
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
		.index-content h1{
			font-size: 1.3rem;
		}
    }
</style>

