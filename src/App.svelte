<script>
	export let name;
	import Snapshot from "./common/Snapshot.svelte";
	import Installation from "./common/Installation.svelte";
	import Tutorial from "./common/Tutorial.svelte";
	import Demopage from "./common/Demopage.svelte";
	import Impression from "./common/Impression.svelte";
	import Intro from "./common/Intro.svelte";

	let whatsClicked = 0;
	function reactor1() {
		whatsClicked = 1;

	};
	function reactor2() {
		whatsClicked = 2;

	};
	function reactor3() {
		whatsClicked = 3;

	};
	function reactor4() {
		whatsClicked = 4;

	};
	function reactor5() {
		whatsClicked = 5;

	};

</script>

<main>
	<div id = "sidebar"> 
		<div on:click = {reactor1} id = "menu1"> 
			Framework info
		</div>
		<div on:click = {reactor2} id = "menu2"> 
			Installation
		</div>
		<div on:click = {reactor3} id = "menu3"> 
			Tutorial
		</div>
		<div on:click = {reactor4} id = "menu4"> 
			Example page
		</div>
		<div on:click = {reactor5} id = "menu5"> 
			My impression
		</div>
	</div>
	<div id = "content">
		{#if whatsClicked == 1}
		<Snapshot />
		{:else if whatsClicked == 2}
		<Installation />
		{:else if whatsClicked == 3}
		<Tutorial />
		{:else if whatsClicked == 4}
		<Demopage />
		{:else if whatsClicked == 5}
		<Impression />
		{:else}
		<Intro />
		{/if}
	</div>
</main>

<style>
	main {
		
		display: flex;
		justify-content: flex-start;
		flex-direction: row;
		font-size:100%;
		padding: 5px;
		margin: none;
		background: rgb(125,201,247);
		background: linear-gradient(90deg, rgba(125,201,247,1) 0%, rgba(182,226,252,1) 7%, rgba(199,233,255,1) 15%, rgba(255,255,255,1) 39%);

	}

	#sidebar {
		display:flex;
		flex-direction: column;
		justify-content: right;
		font-size: 1em;
		padding-top:20px;
		
	
	}
	
	#sidebar div {
		border-bottom-width: thin;
		border-bottom-color: black;
		border-bottom-style: solid;
		padding-left: 0.1em;
		padding-right: 0.3em;
		padding-bottom: 0.1em;

		

	}

	#sidebar div:hover {
		background: rgb(125,201,247, 0.6);

	}


	#content {
		flex-grow: 1;
		padding: 20px;
		background: rgb(255,255,255, 0.7);
		font-size: 0.8em;
	}


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>