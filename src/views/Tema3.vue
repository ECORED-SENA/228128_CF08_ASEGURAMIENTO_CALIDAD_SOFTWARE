<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="zoom-in-left")
      .titulo-principal__numero
        span 3
      h1 Administración de bases de datos

    .row.bg13.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12     
            .row.justify-content-center.align-items-center          
              .col-lg-8.my-3 
                .bg5.brad.px-3.mb-3
                  .row.justify-content-center.align-items-center(data-aos="flip-down")           
                    .col-lg-auto.my-3
                      img.img-a.img-t(src='@/assets/curso/temas/13.png', alt='')       
                    .col.my-3
                      p(data-aos="fade-down").mb-0 Las funciones de un administrador de bases de datos (Data Base Administrator, DBA), es la gestión general de la base de datos. 

                h5.text-white(data-aos="fade-down") Debe conocer las reglas de la tecnología particular, que en este caso sería MySQL, pero también está entre sus responsabilidades:
              .col-lg-4.my-3
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/14.png', alt='')

            .row.justify-content-center.mb-4
              .col-lg-3.my-3.mov
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/15.png', alt='')      
              .col-lg-9.my-3(data-aos="fade-left")
                AcordionA(tipo="a" clase-tarjeta="tarjeta bg7")
                  div(titulo="Validar o revisar el modelado y diseño de las bases de datos")
                    p Debe concentrar su interés en los requerimientos de rendimiento y administración de índices.       

                  div(titulo="Procesos de auditoría")
                    p Identificar qué usuarios tienen acceso a qué tablas o recursos a insertar, actualizar o eliminar datos, y cuándo.      

                  div(titulo="Resguardo y recuperación de datos")
                    p Esto es hacer copias de seguridad periódicas de los datos, mantenerlos a salvo de la destrucción accidental o intencional. Además, diseñar, implementar y probar un plan de recuperación, considerando que pueden presentarse problemas, y validar los datos que se pueden restaurar rápidamente (que las copias generadas sean útiles).     

                  div(titulo="Planificación de capacidad")
                    p Gestionar el volumen de datos y diseñar los planes apropiados para administrarlos, esto ya que los datos crecen rápidamente y se debe llevar un registro de la taza de este crecimiento.     

                  div(titulo="Administración de cambios")
                    p A menudo es la responsabilidad del DBA realizar el análisis de impacto antes de generar los cambios dentro de un SGDB.

            .bg12.brad.p-4.mb-5(data-aos="flip-down")
              p(data-aos="fade-down") De las anteriores actividades, se puede decir que al validar o revisar el modelado y diseño, ya se cuenta con la  competencia para hacerlo, al igual que la administración de cambios, cuando se vio operaciones de mantenimiento y actualización por el MySQL Workbench o por la interfaz línea de comandos.

              p(data-aos="fade-down").mb-0 A continuación, se verá una aproximación sobre cómo hacer y restaurar una copia de la base de datos.


    Separador 
    #t_3_1.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 3.1 Copia de seguridad de base de datos con MySQL Workbench

    p(data-aos="fade-down").mb-5 Durante todo el ciclo de vida del software (desde que se construye hasta que está en operación), se necesitan operaciones de copias y restablecimiento de las bases de datos.  Es por esto que se explicará una de las formas para obtener una copia de la base de datos, tanto en estructura como de los datos:   

      .bg14_1.brad
        .row.justify-content-center.align-items-end.mb-4          
          .col-lg-7.my-3.j
            .p-4
              ul.lista-ul.fa-ul.mb-0                   
                li 
                  i.fas.fa-code.color1
                  | Antes de cualquier cosa, se debe hacer una conexión a la base de datos si no existe dando clic en la casa y luego en el icono más “+”. 
                li 
                  i.fas.fa-code.color1
                  | Posteriormente, en test connection y luego en él se escribe la contraseña del root.
                li 
                  i.fas.fa-code.color1
                  | Se le da doble clic a la conexión creada. 
                li 
                  i.fas.fa-code.color1
                  | Luego, se da clic en la pestaña administración y Data Export. 
                li 
                  i.fas.fa-code.color1
                  | Se debe seleccionar: 
                li                  
                  ul.fa-ul.ps-5
                    li 
                      i.lista-ul__vineta
                      | La base de datos a respaldar.
                    li 
                      i.lista-ul__vineta
                      | Si se va a restaurar la estructura (metadatos) o solo los datos, o solo la estructura (se selecciona estructura y datos).
                    li 
                      i.lista-ul__vineta
                      | La copia en un solo archivo y la ruta.
                    li 
                      i.lista-ul__vineta
                      | Se crea la base de datos si no existe.
                    li.mb-0 
                      i.lista-ul__vineta
                      | Finalmente, en la carpeta se generará el backup. 
              ul.lista-ul.fa-ul.mb-0                   
                li.mb-0 
                  i.fas.fa-code.color1
                  | El proceso termina diciendo que la copia ha terminado.                         
          .col-lg-5         
            img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/16.png', alt='')  

    h5.t1(data-aos="fade-down").mb-5 A continuación, se verá cómo se restablece la copia que se ha generado, usando la herramienta MySQL Workbench.   

    Separador 
    #t_3_2.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 3.2 Restaurar una copia de seguridad con MySQL #[i Workbench]  

    .row.justify-content-center.align-items-center.mb-4           
      .col-lg-7.my-3
        .bg9.p-4.brad.mb-3   
          p(data-aos="fade-down").mb-0 El proceso complementario de restablecer una copia de base de datos es fundamental para la instalación de un sistema o el restablecimiento de la operación, cuando el sistema falla o se quiere volver a una versión anterior de la base de datos. Es por esto que se presentará un método sencillo para restablecer la base de datos a partir de un backup en formato SQL.     
        h5.t1(data-aos="fade-down") Siga los siguientes pasos luego de conectar a la base de datos con MySQL #[i Workbench] como se muestra en la imagen:                  
      .col-lg-5.my-3
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/17.png', alt='')  

    .titulo-sexto.color-acento-contenido
      h5 Figura 16.
      span Pasos 
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t.mb-5(data-aos="zoom-in")(src='@/assets/curso/temas/18.png', alt='Imagen que presenta los pasos luego de conectar a la base de datos con MySQL Workbench.') 

      .row.justify-content-center.align-items-top          
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 1. 
              | Ingrese a la pestaña de administración. 
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 2. 
              | Seleccione Data Import/Restore. 
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 3. 
              | Marque la opción Import from Self-Contained File.    
      .row.justify-content-center.align-items-top          
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 4. 
              | Busque el archivo generado antes.
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 5. 
              | Seleccione la base de datos a restaurar.
        .col-lg.my-1.col-md-12       
          ol.lista-ol.fa-ul
            li 
              span.text-bold 6. 
              | Haga clic en el botón Star Import. 

    p(data-aos="fade-down") Hasta este punto, puede tener la seguridad que está en capacidad de respaldar y restablecer la base de datos por lo menos en un entorno de desarrollo y producción para bases pequeñas. Este proceso le puede servir para bases de datos grandes en las que debe usar la interfaz de comando “línea” con el comando “source”.  Esto debido a que si la copia de seguridad es del tamaño de gigas, MySQL Workbench no podrá abrirlo y puede bloquearse, mientras que por la interfaz de línea de comando, el tamaño de la copia puede ser tan grande como se desee.                                          
</template>

<script>
export default {
  name: 'Tema3',
  data: () => ({
    // variables de vue
  }),
  mounted() {
    this.$nextTick(() => {
      this.$aosRefresh()
    })
  },
  updated() {
    this.$aosRefresh()
  },
}
</script>

<style lang="sass"></style>
