<template>
    <div class="col-12 container-edit">
	<div class="row">
	<div class="col-sm-3 col-3edi">
	<div class="sidebar">
		
		<div class="info">
			<div class="info_content d-flex flex-row align-items-center justify-content-start">
				<h3 class="tituloca">Categorías</h3>
                </div>
		</div>

		<nav class="sidebar_nav">
			<ul>
<li><a href="#">Estéticas, Salones de belleza y Barbería </a><strong class="cant-cate"> (1746)</strong></li>
<li><a href="#">Ferreterías </a><strong class="cant-cate"> (650)</strong></li>
<li><a href="#">Mueblerías, decoración, iluminación y hogar </a><strong class="cant-cate"> (516)</strong></li>
<li><a href="#">Oportunidades en General por caja </a><strong class="cant-cate"> (12390)</strong></li>
<li><a href="#">Papelerías/Mercerías </a><strong class="cant-cate"> (65)</strong></li>
<li><a href="#">Restaurantes </a><strong class="cant-cate"> (33)</strong></li>
<li><a href="#">Sexshop </a><strong class="cant-cate"> (143)</strong></li>
<li><a href="#">Tienda de Abarrotes </a><strong class="cant-cate"> (201)</strong></li>
<li><a href="#">Tienda de Cosméticos/Belleza </a><strong class="cant-cate"> (970)</strong></li>
<li><a href="#">Tienda de Electrónicos </a><strong class="cant-cate"> (1167)</strong></li>
<li><a href="#">Tienda BTCA </a><strong class="cant-cate"> (13)</strong></li>
<li><a href="#">Tienda ETDL </a><strong class="cant-cate"> (23)</strong></li>
<li><a href="#">Tienda ETGN </a><strong class="cant-cate"> (18)</strong></li>
<li><a href="#">Tienda FTMX </a><strong class="cant-cate"> (17)</strong></li>
<li><a href="#">Tienda GTMJ </a><strong class="cant-cate"> (10)</strong></li>
<li><a href="#">Tienda MASS </a><strong class="cant-cate"> (194)</strong></li>
<li><a href="#">Tienda NTGGTP </a><strong class="cant-cate"> (1)</strong></li>
<li><a href="#">Tienda NTNOV </a><strong class="cant-cate"> (43)</strong></li>
<li><a href="#">Tienda TTCS </a><strong class="cant-cate"> (848)</strong></li>
<li><a href="#">Tienda de Mascotas/Veterinaria </a><strong class="cant-cate"> (3)</strong></li>
<li><a href="#">Tienda de Moda y Retail </a><strong class="cant-cate"> (437)</strong></li>
<li><a href="#">Tienda de Regalo, chacharas y novedades </a><strong class="cant-cate"> (510)</strong></li>
				</ul>
		</nav>
</div>
</div>
    <div class="col-sm-9">
	<div class="single-trainer">
		<p id="breadcrumbs"><a href="#">Inicio</a> <strong>»</strong> <a href="#">Todos los productos</a> <strong>»</strong> <strong>Tienda de Electrónicos</strong><!-- pagina1 --></p>
		<h1 class="titulo1">Tienda de Electrónicos</h1>
		<!-- solamente en la pagina principal  -->
		<p id="breadcrumbs2">Computadoras, bocinas, productos de gamers, cables, cámaras, aros de luz, accesorios de celular, celulares.</p>
		<!-- -->
		<p id="breadcrumbs3">Destacados</p>
	 <div class="filter__item">
                        <div class="row">

                          
                            <div class="col-lg-4 col-md-4">
                                <div class="filter__found">
                                    <h6>Mostrando 1–20 de 1167 resultados</h6>
                                </div>
                            </div>
                              <div class="col-lg-4 col-md-5">
                                <div class="filter__sort">
                                    
                                   
                                </div>
                            </div>
                           <div class="col-lg-4 col-md-5">
                                <div class="filter__sort">
                                    
                                    <select>
                                        <option value="0">Ordenar por popularidad</option>
                                        <option value="0">Ordenar por calificación media</option>
                                        <option value="0">Ordenar por los últimos</option>
                                        <option value="0">Ordenar por precio: bajo a alto</option>
                                        <option value="0">Ordenar por precio: alto a bajo</option>
                                    </select>
                                </div>
                            </div>
                        </div>
                    </div>
                     <div class="row">

                   <div class="col-lg-3 col-md-6 col-sm-6" v-for="character in characters.results" :key="character.id">
                            <div class="product__item">
                              
            <div class="meta-text text-sm-center">
            	   <div class="thumb d-flex justify-content-sm-center">
              <img class="img-fluid" alt="Imagen" v-bind:src="character.image">
            </div>
              <h4 class="product__title">{{character.name}}</h4>
              <div class="mb-4">
                <p class="envio-gratis">
                  <i class="fa fa-truck" style="margin-right: 5px;"></i> Envio gratis en México
                </p>
              </div>
          </div>
                            </div>
                        </div>
            
     

     
                    </div>
                     <div class="product__pagination">
                        <a href="#">1</a>
                        <a href="#">2</a>
                        <a href="#">3</a>
                        <a href="#">4</a>
                        <span href="#">..</span>
                        <a href="#">57</a>
                        <a href="#">58</a>
                        <a href="#">59</a>
                        <a href="#"><i class="fa fa-long-arrow-right"></i></a>
                    </div>
	</div>
	</div>	
</div>
</div>
</template>

<script>
import gql from 'graphql-tag'
export default {

    apollo: {
        characters: gql`
        query getCharacters {

            characters {
                results {
                    id
                    name
                    image
                }
            }
        }`
    }
    
}
</script>
<style>

</style>