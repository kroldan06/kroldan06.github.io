<head>
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
  <style>
  .fa {
    padding: 20px;
    font-size: 30px;
    width: 50px;
    text-align: center;
    text-decoration: none;
    margin: 5px 2px;
  }
  
  .fa:hover {
      opacity: 0.7;
  }
  
  .fa-facebook {
    background: #3B5998;
    color: white;
  }
  
  .fa-twitter {
    background: #55ACEE;
    color: white;
  }
  
  .fa-google {
    background: #dd4b39;
    color: white;
  }
  
  .fa-linkedin {
    background: #007bb5;
    color: white;
  }
  
  .fa-youtube {
    background: #bb0000;
    color: white;
  }
  
  .fa-instagram {
    background: #125688;
    color: white;
  }
  
  .fa-pinterest {
    background: #cb2027;
    color: white;
  }
  
  .fa-snapchat-ghost {
    background: #fffc00;
    color: white;
    text-shadow: -1px 0 black, 0 1px black, 1px 0 black, 0 -1px black;
  }
  
  .fa-skype {
    background: #00aff0;
    color: white;
  }
  
  .fa-android {
    background: #a4c639;
    color: white;
  }
  
  .fa-dribbble {
    background: #ea4c89;
    color: white;
  }
  
  .fa-vimeo {
    background: #45bbff;
    color: white;
  }
  
  .fa-tumblr {
    background: #2c4762;
    color: white;
  }
  
  .fa-vine {
    background: #00b489;
    color: white;
  }
  
  .fa-foursquare {
    background: #45bbff;
    color: white;
  }
  
  .fa-stumbleupon {
    background: #eb4924;
    color: white;
  }
  
  .fa-flickr {
    background: #f40083;
    color: white;
  }
  
  .fa-yahoo {
    background: #430297;
    color: white;
  }
  
  .fa-soundcloud {
    background: #ff5500;
    color: white;
  }
  
  .fa-reddit {
    background: #ff5700;
    color: white;
  }
  
  .fa-rss {
    background: #ff6600;
    color: white;
  }
  </style>
  </head>
<h1>Contact</h1>
<style>
    
</style>
<script>
	let times = 1;
	$: message = (`You click me! ${times} times`);


	function onClickMe(event) {
		alert(message);
		times++;
		
	}
</script>

<form>
    <div class="mb-3">
      <label for="exampleInputEmail1" class="form-label">Nombre</label>
      <input type="text" required class="form-control" id="exampleInputNombre1" aria-describedby="NombreHelp">
      <div id="NombreHelp" class="form-text"></div>
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Apellidos</label>
        <input type="text" required class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
        <div id="emailHelp" class="form-text"></div>
      </div>
    <div class="mb-3">
      <label for="exampleInputPassword1" class="form-label">Correo Electrónico</label>
      <input type="email" required class="form-control" id="exampleInputPassword1">
    </div>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Asunto</label>
        <input type="text" required class="form-control" id="exampleInputNombre1" aria-describedby="NombreHelp">
        <div id="NombreHelp" class="form-text"></div>
      </div>
   
   
    <button type="submit">Enviar</button>
    <!--<button on:click={onClickMe}>Enviar</button>-->

  </form>

  <h1>Contactenos</h1>

<a href="#" class="fa fa-facebook"></a>
<a href="#" class="fa fa-twitter"></a>
<a href="#" class="fa fa-google"></a>

<br>

<p>Email: tienda@universal.com</p>
<br>

<li itemscope="" itemtype="http://schema.org/LocalBusiness">
  <span itemprop="telephone"><a href="tel:+50625370000">Teléfono</a></span>
  <span itemprop="name" style="visibility: hidden;">Corporation</span>
</li>		

  
  


 