<template>
	<section class="mensaje-rapido px-3 position-relative">
	    <h3 class="mensaje-rapido__titulo font-weight-bold my-0 py-2 px-3">
	    	{{ titulo }}

	    	<img :src="emoji" alt="Emoji contacto" v-if="emoji" class="mensaje-rapido__emoji">
	    </h3>

	    <div class="h-100 d-flex align-items-center mt-2">
	    	<div>
	    		<slot name="descripcion"></slot>
	    	</div>
	    </div>
    </section>
</template>

<script>
	export default {
		props: {
			titulo: String,
			emoji: String
		}
	}
</script>

<style lang="scss">
.mensaje-rapido {
	border: 3px solid rgba($app-dark, .8);
	padding-top: 2.5rem;
	padding-bottom: 2rem;

	-webkit-box-shadow: 2px 2px 15px -4px rgba(0,0,0,0.75);
	-moz-box-shadow: 2px 2px 15px -4px rgba(0,0,0,0.75);
	box-shadow: 2px 2px 15px -4px rgba(0,0,0,0.75);

	&__titulo {
		font-size: 1.1em;
		color: white;

		background-color: $app-primary;

		border: 2px solid $app-primary;

		position: absolute;
		top: -15px;
		left: 1rem;
	}

	&__emoji {
		width: 1rem;
	}

	p {
		font-size: 1.15em;
	}
}
</style>