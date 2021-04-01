<script>
<<<<<<< HEAD
	export let list=[
		{content:'1',checked:false},
		{content:'2',checked:true},
		{content:'3',checked:false},
	];
	let newItem = ''
	const addNew = ()=>{
		if(newItem==='')return
		list = [...list,{content:newItem,checked:false}]
		newItem = ''
	}
	const remove = (i)=>{
		list = list.filter((_l,index)=>index!==i)
	}
</script>

<main>
	<h1>todo list</h1>
	<input bind:value={newItem} type='text' placeholder='new todo?' />
	<button on:click={addNew}>+</button>
	{#each list as item,i}
	<div>
		<input type="checkbox" bind:checked={item.checked} >
		<span on:click={()=>item.checked = !item.checked} class:checked={item.checked}>{item.content}</span>
		<span on:click={()=>remove(i)}>❌</span>
	</div>
	{/each}
</main>

<style>
	.checked{
		text-decoration: line-through;
	}
=======
	export let name;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
</main>

<style>
>>>>>>> a69e0b5f7c1ce206ec8cb680fd710ca524639525
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>