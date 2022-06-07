<svelte:head>
<title>{title}</title>
</svelte:head>

<script>
	export let title = "Monochrome"
	import { reveal } from 'svelte-reveal';
	import { fly } from 'svelte/transition';
	let visible = {
		projects2022: false,
	};
	let flyx = -40;
</script>

<h1 use:reveal={{ transition: "slide", reset: true, duration: 500 }}>Monochrome</h1>
<projectstitle use:reveal={{ transition: "slide", reset: true, duration: 1000}}>Projects</projectstitle>
<details id="details" use:reveal={{ transition: "slide", reset: true, duration: 3000}} bind:open={visible["projects2022"]}>
	<summary>2022</summary>
	{#if visible["projects2022"]}
		<a href="https://example.com" transition:fly="{{ x: flyx, duration: 500 }}">Not yet</a>
	{/if}
</details>
<profilestitle use:reveal={{ transition: "slide", reset: true, duration: 1000}}>Profiles</profilestitle>
<div class="profile">
	<a use:reveal={{ transition: "slide", reset: true, duration: 1000}} href="https://github.com/graymonochrome">Github</a>
	<a use:reveal={{ transition: "slide", reset: true, duration: 1500}} href="https://gitlab.com/monochrome">Gitlab</a>
	<a use:reveal={{ transition: "slide", reset: true, duration: 2000}} href="https://gitea.misilelaboratory.xyz/monochrome">Gitea</a>
</div>
<donatestitle use:reveal={{ transition: "slide", reset: true, duration: 1000}}>Donate</donatestitle>
<div class="donate">
	<a use:reveal={{ transition: "slide", reset: true, duration: 1500}} href="https://toss.me/monochrom">Toss</a>
</div>

<style>
	#details {
		margin-left: 17.4%;
		font-size: 1.5em;
		color: #ffffff;
	}

	.profile {
		margin-left: 17.4%;
		font-size: 1.5em;
	}

	.donate {
		margin-left: 17.4%;
		font-size: 1.5em;
	}

	profilestitle {
		margin: auto;
		margin-top: 50px;
		margin-left: 17.4%;
		font-size: 1.5em;
		color: #b0b4bc;
	}

	projectstitle {
		display: block;
		color: #b0b4bc;
		font-size: 1.7em;
		margin: auto;
		margin-top: 50px;
		margin-left: 17.4%;
	}

	donatestitle {
		display: block;
		color: #b0b4bc;
		font-size: 1.7em;
		margin: auto;
		margin-top: 50px;
		margin-left: 17.4%;
	}

	h1 {
		color: #70757f;
		font-size: 3em;
		font-weight: 100;
		text-align: center;
		display: block;
		margin: auto;
		margin-top: 10px;
	}

	:global(body) {
		font-weight: 100;
		background-color: #444444;
	}

	a {
		font-weight: 100;
		color: #c7cbd1;
		display: block;
	}
</style>