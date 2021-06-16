<script>
	import { Router, Link, Route } from "svelte-navigator";
	import Home from "./Home.svelte";
	import Product from "./Product.svelte";
	import About from "./About.svelte";
	import Contact from "./Contact.svelte";
	import Carrito from "./Carrito.svelte";
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


<Router>
	<!--<nav>
		<Link to="/">Home</Link>
		<Link to="carrito">Detalle Carrito</Link>
		<Link to="about">About</Link>
		<Link to="contact">Contact</Link> 
	</nav> -->
	<nav class="navbar navbar-default">
		<div class="container-fluid">
		  <!-- Brand and toggle get grouped for better mobile display -->
		  <div class="navbar-header">
			<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
			  <span class="sr-only">Toggle navigation</span>
			  <span class="icon-bar"></span>
			  <span class="icon-bar"></span>
			  <span class="icon-bar"></span>
			</button>
			
		  </div>
	  
		  <!-- Collect the nav links, forms, and other content for toggling -->
		  <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
			<ul class="nav navbar-nav">
				<li class="active"><Link to="/">Home</Link></li>
			  <li ><Link to="carrito">Detalle Carrito</Link></li>
			  <li><Link to="about">About</Link></li>
			  <li><Link to="contact">Contact</Link> </li>
			  
			</ul>
			
		  </div><!-- /.navbar-collapse -->
		</div><!-- /.container-fluid -->
	  </nav>
	<div>
		<Route path="/">
			<Home />
		</Route>
		<Route path="product/*">
			<Route path=":id/:productName/:unitPrice/:unitsInStock/:category/:supplier" component={Product} />
		</Route>
		<Route path="carrito" component={Carrito} />
		<Route path="about" component={About} />
		<Route path="contact" component={Contact} />
	</div>
</Router>