# 09 Creando VISTAS de LOGIN, HOME y PAGINA 404
Practicamente le damos estructura a las paginas

```html
<!-- home -->
<div class="container is-fluid">
    <h1 class="title">Home</h1>
    <h2 class="subtitle">¡Bienvenido usuario!</h2> 
</div>
```
```html
<!-- 404 -->
<div class="main-container">
    <section class="hero-body">
	  	<div class="hero-body">
		    <p class="title">
		      Error 404
		    </p>
		    <p class="subtitle">
		      Pagina no encontrada
		    </p>
	  	</div>
	</section>
</div>
```

```html
<!-- login -->
<div class="main-container">

    <form class="box login" action="" method="POST" autocomplete="off">
		<h5 class="title is-5 has-text-centered is-uppercase">Sistema de inventario</h5>

		<div class="field">
			<label class="label">Usuario</label>
			<div class="control">
			    <input class="input" type="text" name="login_usuario" pattern="[a-zA-Z0-9]{4,20}" maxlength="20" required >
			</div>
		</div>

		<div class="field">
		  	<label class="label">Clave</label>
		  	<div class="control">
		    	<input class="input" type="password" name="login_clave" pattern="[a-zA-Z0-9$@.-]{7,100}" maxlength="100" required >
		  	</div>
		</div>

		<p class="has-text-centered mb-4 mt-3">
			<button type="submit" class="button is-info is-rounded">Iniciar sesion</button>
		</p>
	</form>

</div>
```