<script>
  import { Router, Route, Link } from 'svelte-navigator';
  import { productService } from './product.service';
  let demo = 10;
  let filter = '';
  let filtered = [];

  async function submit() {
    console.log(`Filtering ... ${filter}`);
    const ps = new productService();
    filtered = await ps.search(filter);
  }
</script>
<head>
  <meta charset="utf-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
  <title>Bootstrap 101 Template</title>

  <!-- Bootstrap -->
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css" integrity="sha384-HSMxcRTRxnN+Bdg0JdbxYKrThecOKuH5zCYotlSAcp1+c8xmyTe9GYg1l9a69psu" crossorigin="anonymous">

  <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
  <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
  <!--[if lt IE 9]>
    <script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
    <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
  <![endif]-->
</head>

<h1>Home</h1>

<form on:submit|preventDefault={submit}>
  <input type="search" bind:value={filter} />
  <button type="submit">Search</button>
</form>


{#if filtered && filtered.length > 0}
  <ul>
    {#each filtered as p}
      <li>
        <Link to="product/{p.id}/{p.productName}/{p.unitPrice}/{p.unitsInStock}/{p.category.categoryName}/{p.supplier.companyName}">{p.productName}</Link>
      </li>
    {/each}
  </ul>
{/if}

<h1>Productos</h1>
<ul class="list-group">
  <li class="list-group-item list-group-item-success">OFERTA DEL DIA!!!! Queso</li>
  <li class="list-group-item list-group-item-danger">Computadora DELL (Agotado)</li>
  <li class="list-group-item list-group-item-secondary">Balon de Futbol Adidas</li>
  <li class="list-group-item ">Coca cola</li>
  <li class="list-group-item list-group-item-danger">Headset LG (Agotado)</li>
  <li class="list-group-item list-group-item-warning">Play Station 5  (Descuento)</li>
  <li class="list-group-item list-group-item-info">Uniforme Brasil (Nuevo)</li>
  <li class="list-group-item list-group-item-light">Teclado portatil</li>
  <li class="list-group-item list-group-item-dark">Maquillaje</li>
</ul>



