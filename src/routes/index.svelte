<style>
	h1 {
		text-align: center;
		margin: 0 auto;
	}

	h1 {
		font-size: 0.8em;
		text-transform: uppercase;
		font-weight: 700;
		margin: 0 0 0.5em 0;
	}
	.containerFix {
		height: 1000px;
	}



	@media (min-width: 480px) {
		h1 {
			font-size: 3em;
		}
	}
</style>

<svelte:head>
	<title>Home</title>
</svelte:head>
<main>
<div class="jumbotron">
<div class="embed-responsive embed-responsive-16by9">
	<iframe 
		class="embed-responsive-item" 
		src="https://www.youtube.com/embed/DilHMEovGgY" 
		allowfullscreen
		title="Immore Video">
	</iframe>
</div>
</div>

<h1>Unser Youtubekanal!</h1>	
<div style="height:100px;"></div>

<form>
	<div class="form-group">
	  <label for="exampleInputEmail1">Email address</label>
	  <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
	  <small id="emailHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
	</div>
	<div class="form-group">
	  <label for="exampleInputPassword1">Password</label>
	  <input type="password" class="form-control" id="exampleInputPassword1">
	</div>
	<div class="form-group form-check">
	  <input type="checkbox" class="form-check-input" id="exampleCheck1">
	  <label class="form-check-label" for="exampleCheck1">Check me out</label>
	</div>
	<button type="submit" class="btn btn-primary">Submit</button>
  </form>

  <div class="containerFix"></div>
  <h1>Bis hier kannst du scrollen</h1>
</main>