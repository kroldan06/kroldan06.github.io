<script>
	import { Route, Link } from "svelte-navigator";

	//export let id;
	export let productName;
	export let unitPrice;
	export let unitsInStock;
	export let category;
	export let supplier;

 function myFunction(){
		alert("Al carrito")
	}


</script>

<h2>Product: {productName}</h2>

<p>Precio: </p><a href="/*">{unitPrice}</a>
<br>
<p>Cantidad: </p><a href="/*">{unitsInStock}</a>
<br>
<p>Categoria: </p><a href="/*">{category}</a>
<br>
<p>Proveedor: </p><a href="/*">{supplier}</a>
<br>

<button on:click={myFunction}>Agregar al carrito</button>
