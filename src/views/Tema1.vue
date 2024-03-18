<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="zoom-in-left")
      .titulo-principal__numero
        span 1
      h1 Establecer un entorno de trabajo

    .row.bg2.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12
            .bg1.p-4.brad.mb-5(data-aos="fade-right") 
              .row.justify-content-center.align-items-center           
                .col-lg-3.my-3
                  img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/19.png', alt='')
                .col-lg-7.my-3
                  p(data-aos="fade-down").mb-0 #[b.mark.t3 Es importante saber cómo obtener, instalar, configurar y probar las herramientas necesarias para realizar las operaciones de diseño.] existen muchas tecnologías para diseñar e implementar bases de datos, en este caso, utilizaremos MySQL como sistema gestor de bases de datos y MySQL Workbench como herramienta de diseño, es importante que en la medida que se van presentando los contenidos, realice de forma local y en su computador el trabajo con los ejercicios y ejemplos propuestos.

    Separador 
    #t_1_1.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 1.1 Sistema gestor de bases de datos MySQL

    p(data-aos="fade-down").mb-5 MySQL es un sistema de gestión de bases de datos relacional, desarrollado bajo licencia dual, lo que significa que es una licencia pública general y/o licencia comercial por Oracle Corporation y, que según medios de comunicación, es considerada como la base de datos de código abierto más popular del mundo. Tener licencia dual significa que se puede usar la licencia de uso público sin incurrir en gastos; sin embargo, se puede adquirir una licencia de pago que incluye paquetes que robustecen el producto y servicios de soporte técnico especializado.  

    .row.bg4.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12
            .row.justify-content-center.align-items-center          
              .col-lg-8
                .tarjeta.bg3.p-3.mb-3(data-aos="fade-left")
                  .row.justify-content-around.align-items-center
                    .col-3.col-sm-2.col-lg-auto
                      img.img-t(src="@/assets/curso/temas/8.svg")
                    .col
                      .row.justify-content-between.align-items-center
                        .col.mb-3.mb-sm-0
                          h4.t4.mb-1 Proceso de descarga de MySQL Server Community y MySQL Workbench
                          p.text-white Lo invitamos a visitar el siguiente PDF, para conocer el proceso de descarga de MySQL Server #[i Community] y MySQL #[i Workbench].
                        .col-sm-auto
                          a.boton.color-acento-botones.ts(:href="obtenerLink('/downloads/Proceso_de_descarga_de_MySQL_Server_Community_y_MySQL_Workbench.pdf')" target="_blank")
                            span Descargar
                            i.fas.fa-file-download    

                .tarjeta.bg3.p-3(data-aos="fade-right")
                  .row.justify-content-around.align-items-center
                    .col-3.col-sm-2.col-lg-auto
                      img.img-t(src="@/assets/curso/temas/8.svg")
                    .col
                      .row.justify-content-between.align-items-center
                        .col.mb-3.mb-sm-0
                          h4.t4.mb-1 Proceso de instalación de MySQL 
                          p.text-white Lo invitamos a visitar el siguiente PDF, para conocer el proceso de  instalación de MySQL.
                        .col-sm-auto
                          a.boton.color-acento-botones.ts(:href="obtenerLink('/downloads/Proceso_de_instalacion_de_MySQL_Server_Community.pdf')" target="_blank")
                            span Descargar
                            i.fas.fa-file-download    

    Separador 
    #t_1_2.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 1.2 Sistema de diseño y gestión de bases de datos   

    .row.bg10.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12     
            .row.justify-content-center.align-items-center          
              .col-lg-8.my-3 
                .bg5.brad.p-4.mb-3
                  p(data-aos="fade-down").mb-0 Es una herramienta visual unificada para arquitectos, desarrolladores y administradores de bases de datos. MySQL #[i Workbench] proporciona modelado de datos, desarrollo de SQL y herramientas de administración integrales para la configuración del servidor, administración de usuarios, respaldo y muchas otras características y, lo más importante es que es multiplataforma, lo que indica que puede descargarse para sistemas operativos Windows, Linux y Mac. 

                h5.text-white(data-aos="fade-down") Algunas de las características más importantes de Workbench son las siguientes:                  
              .col-lg-4.my-3
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/9.png', alt='')

            .row.justify-content-center.mb-4
              .col-lg-3.my-3.mov
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/10.png', alt='')      
              .col-lg-9.my-3(data-aos="fade-left")
                AcordionA(tipo="a" clase-tarjeta="tarjeta bg7")
                  div(titulo="Diseño")
                    p MySQL Workbench permite a un administrador de bases de datos, desarrollador o arquitecto de datos diseñar, modelar, generar y administrar bases de datos visualmente. Incluye todo lo que un modelador de datos necesita para crear modelos ER complejos, ingeniería directa e inversa, y también ofrece características clave para realizar tareas difíciles de gestión de cambios y documentación, que normalmente, requieren mucho tiempo y esfuerzo.
                    p En Workbench se pueden crear nuevos modelos, lo que equivale a crear una nueva base de datos e ir agregando los objetos requeridos como tablas, atributos, tipos de datos, relaciones, entre otras.   

                  div(titulo="Desarrollar")
                    p MySQL Workbench ofrece herramientas visuales para crear, ejecutar y optimizar consultas SQL. El editor de SQL proporciona resaltado de sintaxis de color, autocompletado, reutilización de fragmentos de código SQL e historial de ejecución de SQL. El panel de conexiones de base de datos permite a los desarrolladores administrar fácilmente las conexiones de base de datos estándar, incluido MySQL Fabric. El explorador de objetos proporciona acceso instantáneo al esquema y los objetos de la base de datos.  

                  div(titulo="Administrar")
                    p MySQL Workbench proporciona una consola visual para administrar fácilmente los entornos MySQL y obtener una mejor visibilidad de las bases de datos. Los desarrolladores y administradores de bases de datos pueden utilizar las herramientas visuales para configurar servidores, administrar usuarios, realizar copias de seguridad y recuperación, inspeccionar datos de auditoría y ver el estado de la base de datos.  

                  div(titulo="Panel de rendimiento visual")
                    p MySQL Workbench proporciona un conjunto de herramientas para mejorar el rendimiento de las aplicaciones MySQL. Los administradores de bases de datos pueden ver rápidamente los indicadores clave de rendimiento mediante el panel de rendimiento. Los informes de rendimiento proporcionan una fácil identificación y acceso a puntos de acceso de E / S (entrada y salida), declaraciones SQL de alto costo y más. Además, con un clic, los desarrolladores pueden ver dónde optimizar su consulta con el plan visual explain mejorado y fácil de usar.  

                  div(titulo="Migración de bases de datos")
                    p MySQL Workbench proporciona una solución completa y sencilla de usar para migrar Microsoft SQL Server, Microsoft Access, Sybase ASE, PostreSQL y otras tablas, objetos y datos RDBMS a MySQL. Los desarrolladores y administradores de bases de datos pueden convertir rápida y fácilmente las aplicaciones existentes para que se ejecuten en MySQL, tanto en Windows como en otras plataformas. La migración también admite la migración de versiones anteriores de MySQL a las últimas versiones.
    
    
    Separador 
    #t_1_3.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 1.3 Sistemas basados en MySQL    
    .row.justify-content-center.mb-5  
      .col-lg-4.my-3
        .d-grid.h-100
          .crd.bg8.brad.p-4(data-aos="fade-down")
            .crd__text
              p.mb-4 El diseño de un cuestionario está directamente relacionado con el tipo de información que se desea obtener, ya sea información exploratoria o para probar una hipótesis.   
              img.img-t.fr.mov(src='@/assets/curso/temas/11.svg' alt='') 
      .col-lg-4.my-3
        img.img-t.img-a(data-aos="zoom-in")(src='@/assets/curso/temas/12.png', alt='')                             
      .col-lg-4.my-3
        .bg9.p-4.brad.h-100(data-aos="fade-left")
          p(data-aos="fade-down").mb-0 Son instrumentos de investigación que consisten en conjunto de preguntas u otro tipo de indicadores que son diseñados específicamente para recolectar información del usuario encuestado. Esta técnica incluye preguntas cerradas y abiertas, que al final se traducen como herramientas de índole cualitativas o cuantitativas. 

                     
    p(data-aos="fade-down") A continuación, encontrará el PDF Manual de instalación de MariaDB en Windows. En él solo se instala el SGBD, por lo que debe instalar por aparte MySQL Workbench, para que administre las bases de datos de MariaDB. 

    .row.bg11.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12
            .row.justify-content-center.align-items-center          
              .col-lg-8
                .tarjeta.bg3.p-3(data-aos="fade-left")
                  .row.justify-content-around.align-items-center
                    .col-3.col-sm-2.col-lg-auto
                      img.img-t(src="@/assets/curso/temas/8.svg")
                    .col
                      .row.justify-content-between.align-items-center
                        .col.mb-3.mb-sm-0
                          h4.t4.mb-1 Manual de instalación de MariaDB en Windows
                          p.text-white Lo invitamos a visitar el siguiente PDF, para conocer el Manual de instalación de MariaDB en Windows.
                        .col-sm-auto
                          a.boton.color-acento-botones.ts(:href="obtenerLink('/downloads/Manual_de_Instalacion_de_MariaDB_en_Windows.pdf')" target="_blank")
                            span Descargar
                            i.fas.fa-file-download    
</template>

<script>
export default {
  name: 'Tema1',
  components: {},
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
