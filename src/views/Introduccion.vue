<template lang="pug">
.curso-main-container.introduccion
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5.bloque-fondo1
  
    .titulo-principal.color-acento-contenido(data-aos="zoom-in-left")
      .titulo-principal__numero
        span
          i.fas.fa-info
      h1 Introducción
    
    .row.justify-content-center 
      .col-lg-10    
        .row.justify-content-center.align-items-center.mb-4         
          .col-lg-4.my-3
            img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/2.png', alt='')     

          .col-lg-8.my-3
            .bg28.brad.p-4
              h5(data-aos="fade-down") #[mark.t3.px-2 Bienvenido al presente componente formativo]
              p(data-aos="fade-down") Una vez definidos los conceptos básicos de las bases de datos, se está listo para afrontar su análisis y diseño, el cual consiste en tomar los datos más importantes que están implicados en un problema o qué datos son necesarios para llevar el control por un sistema informático a implementar. 

              p(data-aos="fade-down") Para extraer los datos, se debe hacer un análisis detallado del problema, para poder descartar los que no son susceptibles a la administración por el sistema a desarrollar, luego de tener extraídos los datos esenciales, se puede empezar a construir el modelo adecuado, por lo que se necesitará una herramienta de diseño de base datos y a través de ella expresar todos los aspectos técnicos de la solución a implementar.          

        .row.justify-content-center.align-items-center.px-3.bg17.brad(data-aos="flip-down")           
          .col-lg-auto.beat.my-3
            img.img-a.img-t(src='@/assets/curso/temas/3.svg', alt='')       
          .col.my-3.text-white
            p(data-aos="fade-down") Este componente brinda una serie de ejercicios prácticos de análisis y diseño, a la vez que profundiza en los temas de modelado.

            h5(data-aos="fade-down").mb-0 Le deseamos muchos éxitos en este proceso de aprendizaje.


</template>

<script>
export default {
  name: 'Introduccion',
  data: () => ({
    // variables de vue
  }),
}
</script>

<style lang="sass"></style>
