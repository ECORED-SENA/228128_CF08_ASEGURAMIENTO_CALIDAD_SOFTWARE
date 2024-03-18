<template lang="pug">
.curso-main-container.pb-3
  BannerInterno
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5.mb-5
    .titulo-principal.color-acento-contenido(data-aos="zoom-in-left")
      .titulo-principal__numero
        span 2
      h1 Ejercicios de diseño e implementación

    .row.bg14.align-items-center(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12
            .bg1.p-4.brad.mb-5(data-aos="fade-right") 
              .row.justify-content-center.align-items-center           
                .col-lg-3.my-3
                  img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/19.png', alt='')
                .col-lg-7.my-3
                  p(data-aos="fade-down").mb-0 El aprendizaje basado en problemas es una buena estrategia a seguir en este tipo de actividades, debido a que es el análisis de un problema el que da origen a un modelo de base de datos. Por lo tanto, se propondrán dos problemas a considerar, y en torno a ellos se van reforzando los conocimientos adquiridos a la vez que se va profundizando en algunos conceptos. Para lograrlo, se toma como problema los casos comunes como lo son el análisis y diseño de un sistema de facturación en inventarios y un sistema para gestionar las matrículas de estudiantes en un instituto de formación técnica.

    Separador 
    #t_2_1.titulo-segundo.color-acento-contenido.mb-3(data-aos="zoom-in-left")
      h2 2.1 Análisis y diseño sistema de facturación       

    .row.bg13.align-items-center.mb-5(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12     
            .row.justify-content-center.align-items-center          
              .col-lg-8.my-3
                p(data-aos="fade-down") Analicemos el primer caso, llamado Sistema de facturación.

                .bg9.brad.px-3.mb-3
                  .row.justify-content-center.align-items-center(data-aos="flip-down")           
                    .col-lg-auto.my-3
                      img.img-a.img-t(src='@/assets/curso/temas/20.png', alt='')       
                    .col.my-3
                      p(data-aos="fade-down").mb-0 Suponga que lo contratan para diseñar una base de datos de una droguería, el objetivo principal es llevar las existencias de cada producto, a la vez que se va facturando lo que se vende, también interesa la información de los clientes, porque a futuro se quiere hacer campañas publicitarias de email marketing, según los productos que cada cliente consume.

                h5.text-white.mb-4(data-aos="fade-down") En una entrevista, el cliente dijo que necesitaba algunos reportes como: 

                .bg6.brad.p-4.mb-4
                  .row.justify-content-center 
                    .col-lg-3.my-3
                      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/22.png', alt='')                            
                    .col-lg-9.my-3
                      .bg15.brad.h-100.p-3.j        
                        ol.lista-ol--cuadro.fa-ul.mb-0
                            li 
                              .lista-ol--cuadro__vineta
                                span 1
                              | Artículo más vendido.
                            li 
                              .lista-ol--cuadro__vineta
                                span 2
                              | Artículos que más utilidades dejan por unidad.
                            li 
                              .lista-ol--cuadro__vineta
                                span 3
                              | Empresa o persona que más factura (cantidad de factura).
                            li 
                              .lista-ol--cuadro__vineta
                                span 4
                              | Empresa o persona que más factura (volumen de ventas en pesos).
                            li.mb-0 
                              .lista-ol--cuadro__vineta
                                span 5
                              | Productos sin existencia.    
                 
              .col-lg-4.my-3
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/21.png', alt='')  

            p.text-white(data-aos="fade-down") También fijó los productos que se organizan por categoría, porque le interesa saber el precio de compra y de venta, para conocer qué descuento hacer a una factura.

            h5.t4.text-white.my-4(data-aos="fade-down") El cliente ofrece un modelo sobre cómo debe ser la factura, como se muestra en la siguiente figura.
            .titulo-sexto.color-acento-contenido.text-white
              h5 Figura 1.
              span Modelo de factura 
            .bg6.brad.p-4.mb-5
              img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/23.png', alt='Imagen que presenta un modelo de factura para el caso que se está estudiando.')  

    .row.justify-content-start.mb-4 
      .col-auto(data-aos="flip-down")
        .list
          .list__item
            .list__item__icon
              img(src='@/assets/curso/temas/icon.svg', alt='')
          .list__txt.bgicon.p-0.px-4
            h3.mb-0 Análisis y diseño               


    .row.bg16.align-items-center.mb-5(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12                          
            .row.justify-content-center.mb-5  
              .col-lg-4.my-3
                .bg9.brad.h-100.p-4(data-aos="fade-down")
                  p(data-aos="fade-down") Una buena forma de empezar el análisis es con el formato de la factura; se inicia revisando la cabecera de la factura. 

                  p(data-aos="fade-down").mb-0 Un primer impulso puede hacer pensar que se debe crear una entidad para la compañía o empresa y pensar en definir una entidad o empresa con atributos “nombre_compañia”, “direccion”, “ciudad”, etc.; sin embargo, considere lo siguiente:
              .col-lg-4.my-3
                img.img-t.img-a(data-aos="zoom-in")(src='@/assets/curso/temas/24.png', alt='')                             
              .col-lg-4.my-3
                .bg8.p-4.brad.h-100(data-aos="fade-left")
                  p(data-aos="fade-down").mb-0 El cliente le ha pedido que modele un sistema de facturación para su droguería, es decir, para una droguería, no para un conjunto de droguerías.  Es diferente si solicitaran “se necesita un sistema de facturación que administre el inventario y facturación de múltiples droguerías”, a estos problemas se les llama multitenant (multiinquilino), pero este no es el caso. Por lo tanto, no es la entidad droguería parte del modelo, porque no se está modelando la facturación de múltiples droguerías.   

            .titulo-sexto.color-acento-contenido.text-white
              h5 Figura 2.
              span Factura con información resaltada
            .bg6.brad.p-4.mb-5
              img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/25.png', alt='Imagen que resalta en la factura, la información que se presenta del cliente.')    

    p(data-aos="fade-down") Tal parece que los datos más relevantes de los clientes están presentados en la parte resaltada de la imagen, lo que hace pensar que se requiere una entidad, cliente, usuario o persona y, que la persona puede tener relacionada una empresa o tal vez una persona hace la compra para una empresa.

    .row.justify-content-center.align-items-center          
      .col-lg-8.my-3 
        .bg5.brad.px-3.mb-3
          .row.justify-content-center.align-items-center(data-aos="flip-down")           
            .col-lg-auto.my-3
              img.img-a.img-t(src='@/assets/curso/temas/26.png', alt='')       
            .col.my-3
              p(data-aos="fade-down").mb-0 Lo anterior se puede modelar con una entidad, la entidad persona que relaciona los datos (nombre, compañía, dirección, ciudad, teléfono, correo electrónico).   
        p(data-aos="fade-down") Una forma simplificada sería creando una entidad persona y para poder identificar cada fila usar una llave primara (id_persona), pero también es importante usar un identificador único de persona como lo es el documento de identificación (porque las personas nunca tienen el mismo número), de igual forma, debe tener en cuenta que no puede existir una persona si al menos no se define el número de identificación y el nombre. 
        h5.t1(data-aos="fade-down") Lo anterior se puede ver en la siguiente imagen (flecha roja para definir la llave primaria, morada para definir los datos que deben ser registrados obligatoriamente, y la verde una columna cuyo valor no puede repetirse en toda la tabla).
      .col-lg-4.my-3
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/27.png', alt='')          

    .titulo-sexto.color-acento-contenido
      h5 Figura 3.
      span Identificación 
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/28.png', alt='Imagen que presenta en qué parte se define la llave primaria, los datos que deben ser registrados obligatoriamente y el valor que no puede repetirse en toda la tabla.')

    p(data-aos="fade-down").mb-5 Tal parece que los datos más relevantes de los clientes están presentados en la parte resaltada de la imagen, lo que hace pensar que se requiere una entidad, cliente, usuario o persona y, que la persona puede tener relacionada una empresa o tal vez una persona hace la compra para una empresa.

    .titulo-sexto.color-acento-contenido
      h5 Figura 4.
      span Creación de tabla con las compañías 
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/29.png', alt='Imagen que presenta la creación de una tabla cuando son varias compañías.')

    h5.t1(data-aos="fade-down").mb-5 Como hay menos compañías que personas, se ha tomado id_compania como SMALLINT. Esta decisión permite cumplir con dos requerimientos no funcionales: 

    .row.justify-content-center.align-items-center          
      .col-lg-4.my-3 
        .bg17.brad.px-3.mb-3.text-white
          .row.justify-content-center.align-items-center(data-aos="flip-down")           
            .col-lg-auto.my-3
              img.img-a.img-t(src='@/assets/curso/temas/30.png', alt='')       
            .col.my-3
              p(data-aos="fade-down").mb-0 Ahorro de espacio de almacenamiento.     

      .col-lg-4.my-3 
        .bg9.brad.px-3.mb-3
          .row.justify-content-center.align-items-center(data-aos="flip-down")           
            .col-lg-auto.my-3
              img.img-a.img-t(src='@/assets/curso/temas/31.png', alt='')       
            .col.my-3
              p(data-aos="fade-down").mb-0 Ahorro en el tiempo computacional de las consultas.    

      .col-lg-8
        .row.justify-content-center.align-items-center.px-3.bg18.brad(data-aos="flip-down")           
          .col-lg-auto.beat.my-3
            img.img-a.img-t(src='@/assets/curso/temas/3.svg', alt='')       
          .col.my-3
            H4(data-aos="fade-down") Nota: 
            p(data-aos="fade-down").mb-0 Es importante comprender cómo la decisión de tipo de dato apunta a cumplir con los requerimientos no funcionales. 
            
    h5.t1(data-aos="fade-down").my-5 Es posible que piense que debe haber una relación entre la persona y la compañía de la siguiente forma:      

    .titulo-sexto.color-acento-contenido
      h5 Figura 5.
      span Relación entre la persona y la compañía 
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/32.png', alt='Imagen que presenta la relación entre la persona y la compañía.')

    p(data-aos="fade-down") Al hacerlo de esta forma, una persona puede pertenecer a una empresa (solo a una), pero esa misma persona podría comprar en la farmacia unas veces a nombre propio y otras a nombre de la empresa, y este modelo no permitiría saber cada caso. Otro problema es que esa persona un día compra a nombre de una empresa y otro día puede comprar a nombre de otra empresa (si cambia de empresa) y al actualizar la empresa de la persona, se estarían actualizando las facturas pasadas, lo cual sería un error. 
    h5.t1(data-aos="fade-down").mb-5 De esta forma, la manera correcta sería relacionar la persona y la empresa con la factura. 

    .titulo-sexto.color-acento-contenido
      h5 Figura 6.
      span Información de la factura
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/33.png', alt='Imagen que presenta resaltada, la información de la factura.')  

    .row.justify-content-center.align-items-center          
      .col-lg-8.my-3
        p(data-aos="fade-down") Ahora, se presentan los datos de la factura y sus datos, como número de factura (que debe ser único y secuencial), fecha, la identificación del cliente (código interno id_persona), y términos de pago. 
        .bg17.brad.p-4.mb-3
          p(data-aos="fade-down").mb-0.text-white Como se puede ver en la siguiente imagen, se creó la tabla término de pago, que almacenará los medios de pago (crédito, contado, contra entrega, etc.), note también que se usó el tipo de datos TINYTINT que solo almacena números de 0-126 y se hace una relación de 1 a muchos (un término puede tener relacionadas muchas facturas, o lo que es igual muchas facturas tienen un mismo término de pago).
        
      .col-lg-4.my-3
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/34.png', alt='') 

    .titulo-sexto.color-acento-contenido
      h5 Figura 7.
      span Creación de la tabla término de pagos
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/35.png', alt='Imagen que presenta la creación de la tabla término de pago.')    

    .row.justify-content-center.mb-5  
      .col-lg-4.my-3
        .bg8.p-4.brad.h-100.j(data-aos="fade-left")
          p(data-aos="fade-down").mb-0 Note que una factura necesariamente debe tener relacionada la referencia de una persona, el término, la fecha y la hora, pero la compañía (id_compania) no es obligatoria. Esto es porque hay facturas que las compran las personas naturales y otras que las compran las empresas o compañías, pero en un caso o en el otro, siempre habrá una persona que hace la compra, es por esto que el id_persona es obligatoria.  
      .col-lg-4.my-3
        img.img-t.img-a(data-aos="zoom-in")(src='@/assets/curso/temas/36.png', alt='') 
      .col-lg-4.my-3
        .d-grid.h-100
          .crd.bg9.brad.p-4(data-aos="fade-down")
            .crd__text
              p.mb-4 La factura tiene un tipo de dato BIGINT, porque se espera que pueda facturar muchos al ser minorista, note también la columna AI (Auto Incrementable), esto hace que el gestor de base datos le asigne automáticamente y secuencialmente un número a cada fila para la columna id_factura.
              img.img-t.fr.mov(src='@/assets/curso/temas/37.png' alt='')  

    h5.t1(data-aos="fade-down").mb-5 Otro segmento de la factura son los ítems o productos que la componen:

    .titulo-sexto.color-acento-contenido
      h5 Figura 8.
      span Ítems que componen la factura
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/38.png', alt='Imagen que presenta los ítems o productos que componen la factura.') 

    h5.t1(data-aos="fade-down").mb-5 La imagen sugiere que los productos tienen una descripción, un precio unitario y como mencionó el cliente, un precio de compra:  

    .titulo-sexto.color-acento-contenido
      h5 Figura 9.
      span Apartados que tienen los productos
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/39.png', alt='Imagen que presenta los apartados que tienen los productos.') 
    p(data-aos="fade-down").mb-5 Una categoría puede tener varios productos o varios productos pertenecen a una categoría, esto es una relación de 1 a muchos, que queda definida en la imagen anterior. Note los tipos de datos definidos y también que la columna existencia no puede ser null, además de eso, si el usuario no pone un dato o trata de poner dato null en la existencia, entonces el sistema gestor de base de datos le pondrá “0” a esa fila en esa columna.  La imagen sugiere que los productos tienen una descripción, un precio unitario y como mencionó el cliente, un precio de compra:       

    .row.justify-content-center.align-items-center          
      .col-lg-7.my-3
        .bg9.brad.px-3.mb-3
          .row.justify-content-center.align-items-center(data-aos="flip-down")           
            .col-lg-auto.my-3
              img.img-a.img-t(src='@/assets/curso/temas/40.png', alt='')       
            .col.my-3
              p(data-aos="fade-down").mb-0 Ahora, resta relacionar los productos con la factura, y una factura puede relacionar varios productos, y un mismo producto puede estar en muchas facturas, por lo tanto, es una relación de muchos a muchos (n:m), esto hace que se genere una entidad intermedia que se llama producto_factura.  
        p(data-aos="fade-down") La usabilidad es una medida de calidad que busca medir la eficacia, eficiencia y satisfacción en la experiencia del usuario con respecto a un producto, lo ideal es que este tipo de interacción entre usuario/producto sea lo más fácil y simple posible. 
      .col-lg-5.my-3
        img.img-a.img-t(src='@/assets/curso/temas/41.png', alt='') 

    .titulo-sexto.color-acento-contenido
      h5 Figura 10.
      span Filas
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/42.png', alt='Imagen que muestra cada fila y su representación.') 
    p(data-aos="fade-down").mb-5 La entidad factura_producto es una relación de muchos a muchos y agrega los datos necesarios para saber en cuánto y cuántos productos se venden por factura. También en la siguiente imagen se muestra cómo son obligatorias todas las columnas de este modelo y que la cantidad por defecto tiene valor de 1, debido a que si se intenta guardar un valor nulo, no debe ser posible y en lugar de insertar nulo insertará 1, porque no tiene sentido agregar un producto a una factura y no vender al menos un producto.                  

    .titulo-sexto.color-acento-contenido
      h5 Figura 11.
      span Columnas del modelo
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/43.png', alt='Imagen que presenta las columnas del modelo explicado.') 

    Separador 
    #t_2_2.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 2.2 Identificación de sentencias DDL   

    .row.bg19.align-items-center.mb-5(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12     
            .row.justify-content-center.align-items-center 
              .col-lg-4.my-3
                img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/45.png', alt='')                        
              .col-lg-8.my-3
                .bg5.brad.px-3.mb-3
                  .row.justify-content-center.align-items-center(data-aos="flip-down")           
                    .col-lg-auto.my-3
                      img.img-a.img-t(src='@/assets/curso/temas/46.png', alt='')       
                    .col.my-3
                      p(data-aos="fade-down").mb-0 Suponga que lo contratan para diseñar una base de datos de una droguería, el objetivo principal es llevar las existencias de cada producto, a la vez que se va facturando lo que se vende, también interesa la información de los clientes, porque a futuro se quiere hacer campañas publicitarias de email marketing, según los productos que cada cliente consume.

                p(data-aos="fade-down") MySQL Workbench ofrece la interfaz gráfica con la que se pueden generar estos códigos. Se mostrará cómo se hace con algunos ejemplos, siga los siguientes pasos:  

            .tarjeta.tarjeta--gris.p-4.mb-5(data-aos="fade-left")
              SlyderA(tipo="b")
                .row.justify-content-center.align-items-center.p-2
                  .col-lg-5.my-3.col-md-auto
                    h5 #[mark.bgtg.brad2.px-2 1]
                    .t5.pe-5
                      p Haga clic derecho a la entidad persona y luego a “Copy to Clipboard” (copiar SQL en portapapeles).  
                  .col-lg-5.my-3.mb-4.mb-md-0
                    img.img-a.img-t(src='@/assets/curso/temas/48.png', alt="")  
                 
                .row.justify-content-center.align-items-center.p-2
                  .col-lg-5.my-3.col-md-auto
                    h5 #[mark.bgtg.brad2.px-2 2]
                    .t5.pe-5
                      p Después se debe pegar (Ctrl+V) el contenido en un editor de texto y el resultado será: 
                  .col-lg-5.my-3.mb-4.mb-md-0
                    img.img-a.img-t(src='@/assets/curso/temas/49.png', alt="")                   
         
            p(data-aos="fade-down") Como puede apreciar, es posible obtener la definición de la base de datos en lenguaje SQL (DDL), si no se tuviera MySQL Workbench, se tendría que elaborar cada una de las sentencias.

            h5(data-aos="fade-down") Pruebe sus conocimientos a través del siguiente ejercicio, en el que identifique en la sintaxis:   

            .row.justify-content-center.align-items-center          
              .col-lg-4.my-3 
                .bg9.brad.px-3.mb-3
                  .row.justify-content-center.align-items-center(data-aos="flip-down")           
                    .col-lg-auto.my-3
                      img.img-a.img-t(src='@/assets/curso/temas/50.png', alt='')       
                    .col.my-3
                      p(data-aos="fade-down").mb-0 Cómo en SQL define una llave primaria.    

              .col-lg-4.my-3 
                .bg9.brad.px-3.mb-3
                  .row.justify-content-center.align-items-center(data-aos="flip-down")           
                    .col-lg-auto.my-3
                      img.img-a.img-t(src='@/assets/curso/temas/51.png', alt='')       
                    .col.my-3
                      p(data-aos="fade-down").mb-0 Cómo en SQL se define un índice único.  

              .col-lg-8
                p(data-aos="fade-down").mb-4 Es importante que se familiarice con estas sentencias, porque las operaciones de mantenimiento de bases de datos como adición o sustracción de columnas o tablas, son más fáciles cuando se hacen a través de la ejecución de scripts en lenguaje SQL.              
              .col-lg-8
                .row.justify-content-center.align-items-center.px-3.bg3.brad(data-aos="flip-down")           
                  .col-lg-auto.beat.my-3
                    img.img-a.img-t(src='@/assets/curso/temas/3.svg', alt='')       
                  .col.my-3.text-white
                    H4(data-aos="fade-down") Nota: 
                    p(data-aos="fade-down").mb-0 Como no se ha especificado el nombre de la base de datos MySQL Workbench pone por defecto `mydb` a la base de datos.     

            h5(data-aos="fade-down").my-5 A continuación, se presenta una entidad más compleja, como lo es la entidad factura:   
            .bg3.brad
              .row.justify-content-center.align-items-end          
                .col-lg-6.my-3
                  .p-4 
                    .bg20.brad.p-4
                      p.ps-3 #[b CREATE TABLE IF NOT EXISTS] `mydb`.`factura` ( 
                      p.ps-1 `id_factura` #[b BIGINT NOT NULL AUTO_INCREMENT],
                      p.ps-1 `id_persona` #[b INT NOT NULL,]
                      p.ps-1 `id_compania` #[b SMALLINT NULL,]
                      p.ps-1 `id_termino` #[b TINYINT NOT NULL,]
                      p.ps-1 `fecha` #[b DATE NOT NULL,]
                      p.ps-1 `hora` #[b TIME NOT NULL,]
                      p.ps-1 #[b PRIMARY KEY] (`id_factura`),
                      p.ps-1 #[b INDEX] `fk_factura_persona_idx` (`id_persona` #[b ASC]) #[b VISIBLE,]
                      p.ps-1 #[b INDEX] `fk_factura_compania1_idx` (`id_compania` #[b ASC]) #[b VISIBLE,]
                      p.ps-1 #[b INDEX] `fk_factura_termino1_idx` (`id_termino` #[b ASC]) #[b VISIBLE,]
                      p.ps-1 #[b CONSTRAINT] `fk_factura_persona`
                      p.ps-3 #[b FOREIGN KEY] (`id_persona`)
                      p.ps-3 #[b REFERENCES] `mydb`.`persona` (`id_persona`)
                      p.ps-3 #[b ON DELETE NO ACTION]
                      p.ps-3 #[b ON UPDATE NO ACTION,]
                      p.ps-1 #[b CONSTRAINT] `fk_factura_compania1`
                      p.ps-3 #[b FOREIGN KEY] (`id_compania`)
                      p.ps-3 #[b REFERENCES] `mydb`.`compania` (`id_compania`)
                      p.ps-3 #[b ON DELETE NO ACTION]
                      p.ps-3 #[b ON UPDATE NO ACTION,]
                      p.ps-1 #[b CONSTRAINT] `fk_factura_termino1`
                      p.ps-3 #[b FOREIGN KEY] (`id_termino`)
                      p.ps-3 #[b REFERENCES] `mydb`.`termino` (`id_termino`)
                      p.ps-3 #[b ON DELETE NO ACTION]
                      p.ps-3 #[b ON UPDATE NO ACTION])
                      p ENGINE = InnoDB   

                .col-lg-6
                  img.img-a.img-t(src='@/assets/curso/temas/52.png', alt='')  

            h5(data-aos="fade-down").my-5 Observe cómo las llaves foráneas les define un índice:                        
            .row.justify-content-center.mb-5     
              .col-lg-8
                .bgtg.text-center.brad.p-3.mb-4(data-aos="fade-down")
                  p.mb-0 #[b INDEX] `fk_factura_persona_idx` (`id_persona` #[b ASC]) #[b VISIBLE],             
                p(data-aos="fade-down") Con esta sintaxis, lo que hace MySQL #[i Workbench] es decirle al gestor de base de datos MySQL que esta columna id_persona debe guardarse en estructura de árbol binario (que se llame fk_factura_persona_idx) y no de manera secuencial.  Este tipo de estructura de datos en árbol mejora la velocidad de las operaciones de consulta y búsqueda.

                p(data-aos="fade-down") También se crean índices para las columnas id_compania e id_termino.
                .row.justify-content-center.align-items-center.px-3.bg3.brad(data-aos="flip-down")           
                  .col-lg-auto.beat.my-3
                    img.img-a.img-t(src='@/assets/curso/temas/3.svg', alt='')       
                  .col.my-3.text-white
                    H4(data-aos="fade-down") Nota: 
                    p(data-aos="fade-down").mb-0 Usar MySQL #[i Workbench] ayuda a definir la estructura de almacenamiento de los datos para que cumpla con el requerimiento no funcional de rendimiento en las consultas. 

            p(data-aos="fade-down").mb-5 También MySQL WorKbench crea unas restricciones que permiten mantener la integridad de los datos.                       
            .row.justify-content-center.mb-5     
              .col-lg-8
                .bgtg.brad.px-4.mb-4
                  .row.justify-content-center.align-items-end         
                    .col-lg-8.my-3
                      p #[b CONSTRAINT] `fk_factura_persona`
                      p.ps-3 #[b FOREIGN KEY] (`id_persona`)
                      p.ps-3 #[b REFERENCES] `mydb`.`persona` (`id_persona`)
                      p.mb-0.ps-3 #[b ON DELETE NO ACTION] ACTION,]
                    .col-lg-4
                      img.img-a.img-t(src='@/assets/curso/temas/53.png', alt='')       

            h5(data-aos="fade-down").mb-5 A continuación, se presenta línea a línea, recordando que la columna id_persona es una llave foránea de la tabla persona:

            .titulo-sexto.color-acento-contenido
              h5 Tabla 1.
              span Restricciones

            .tabla-a.color-acento-contenido.mb-5(data-aos="fade-left") 
              table
                thead.bgh    
                  tr
                    th.brth Nombre restricción 
                    th.brth Descripción 
                tbody.bgt
                  tr
                    td.brt #[b CONSTRAINT] `fk_factura_persona`   
                    td.brt Indica al SGDB que debe crear una restricción (#[i CONSTRAINT]) que se llama fk_factura_persona 
                  tr
                    td.brt #[b FOREIGN KEY] (`id_persona`)
                    td.brt Indica la columna  que es llave foránea, es decir, que id_persona es una referencia de una fila de otra tabla.
                  tr
                    td.brt #[b REFERENCES] `mydb`.`persona` (`id_persona`)
                    td.brt La fila de la otra tabla de la que es referencia de la base de datos mydb, tabla persona columna id_persona
                  tr
                    td.brt #[b ON DELETE NO ACTION]
                    td.brt Qué acción debe hacer el SGDB si borran la fila de la tabla persona con los datos de la tabla factura que estén relacionados, acá dice que no le permite borrar personas que ya tienen facturas.
                  tr
                    td.brt #[b ON UPDATE NO ACTION,]
                    td.brt Qué acción debe hacer el SGDB si actualiza la columna id_persona una fila de la tabla persona con los datos de la tabla factura que estén relacionados, acá dice que no le permita actualizar la columna id_persona de la tabla persona que ya tiene facturas.      

            p(data-aos="fade-down") No es de preocuparse si no es muy claro hasta la decisión del SQL de llaves foráneas, dado que a lo largo de la práctica y la revisión del material complementario, podría complementar los diferentes elementos y conceptos.       

    Separador 
    #t_2_3.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 2.3 Generar la base de datos

    p(data-aos="fade-down") A continuación, se presentará cómo obtener el modelo físico de una base de datos en formato natural de las bases de datos (esto es SQL). Con el siguiente procedimiento se obtendrá un modelo de datos en sentencias DDL, en un uno archivo con extensión .sql., estos documentos son los códigos fuente de las bases de datos, generalmente en el proceso de desarrollo de software son versionados como cualquier archivo de código fuente.

    h5.t1.mb-5(data-aos="fade-down") De acuerdo con lo anterior, una forma de generar la base de datos es la siguiente:         

    .bg22.mb-4
      .row.justify-content-center.align-items-center
        .col-lg-4
          img.img-a.img-t.mov(data-aos="zoom-in")(src='@/assets/curso/temas/55.png', alt='')      
        .col-lg-7.my-4(data-aos="fade-left")    
          SlyderF.px-3(columnas="col-lg-6")
            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/57.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 1
                  | Ponga un nombre a la base de datos dando clic derecho en editar Schema.       

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/58.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 2
                  span Seleccione Ingeniería hacia adelante (#[i Forward Ingingger]).

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/59.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 3
                  span Entre los datos de #[i root] base de datos.

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/60.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 4
                  | Seleccione las opciones de la base de datos y se deja por defecto.

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/61.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 5
                  span Luego, pide la contraseña de usuario #[i root] que se puso en el proceso de instalación de MySQL.

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/62.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 6
                  | Después muestra un resumen de lo que creará.

            .tarjeta.bgs.p-4
              img.img-a.img-t.mb-2(src='@/assets/curso/temas/63.png', alt='')
              ol.lista-ol--cuadro.fa-ul.mb-0
                li 
                  .lista-ol--cuadro__vineta.color2
                    span 7
                  span Finalmente, le da en #[i Next] y el sistema generará el DDL de la base datos.

    p(data-aos="fade-down") Se guarda un archivo #[b.t1 “Save to file”] y se copia al portapapeles #[b.t1 “Copy to clipboard”]. Se sugiere antes de dar #[i Next] y continuar el proceso, primero guardar como un archivo y ponerle este nombre, luego de ponerlo le da #[i Next] para que ejecute ese script en el SGDB instalado.  

    .row.justify-content-center.align-items-center          
      .col-lg-9.my-3
        .bg17.brad.p-4
          p(data-aos="fade-down").mb-0.text-white El archivo generado guardado en formato de texto con extensión .sql es lo que se llama el script DDL de la base de datos, es el principal producto de un modelo de datos, es el entregable de un proyecto y por lo que materialmente se puede pasar una factura al cliente. 
        
      .col-lg-3.my-3
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/64.png', alt='') 

    Separador 
    #t_2_4.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 2.4.	Operaciones de mantenimiento y actualización 

    .row.justify-content-center.mb-5  
      .col-lg-4.my-3
        .bg9.brad.h-100.p-4(data-aos="fade-down")
          p(data-aos="fade-down").mb-0 Por lo general, la base datos se diseña y se despliega en servidores en la nube, hosting o en instancias de almacenamiento, sistemas operativos o de plataforma que no tienen interfaz gráfica, es por eso que es importante el archivo de texto DDL con extensión .sql, la base de datos hasta ahora generada presenta una inexactitud que se ha puesto para ejemplificar una operación de actualización o mantenimiento.
      .col-lg-4.my-3
        img.img-t.img-a(data-aos="zoom-in")(src='@/assets/curso/temas/65.png', alt='')                             
      .col-lg-4.my-3
        .bg8.p-4.brad.h-100(data-aos="fade-left")
          p(data-aos="fade-down").mb-0 Suponga que el cliente ha contratado un servidor en la nube para la base de datos y al darle subir el archivo de extensión .sql ha generado la base de datos, pero, se ha dado cuenta que su modelo está mal o incompleto y lleva varios meses trabajando la base de datos, hay muchos datos, por lo que no se puede volver a empezar con una base de datos vacía, sino que se debe ajustar la base de datos actual (base en producción) sin borrar o alterar los datos que la base ya tiene.

    p(data-aos="fade-down") Además, junto a su equipo de trabajo ha detectado que no modelaron el pie de la factura:    

    .titulo-sexto.color-acento-contenido
      h5 Figura 12.
      span Pie de la factura
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/66.png', alt='Imagen que presenta el pie de la factura que se viene trabajando.') 
    p(data-aos="fade-down") Este ajuste consiste en agregar en la tabla factura, el valor del subtotal y la tasa de impuesto a aplicar; con estos datos se puede calcular el total:   

    .titulo-sexto.color-acento-contenido
      h5 Figura 14.
      span Información a agregar en la tabla factura
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/67.png', alt='Imagen que presenta el pie de la factura que se viene trabajando.') 
    p(data-aos="fade-down").mb-5 Ahora, se necesitan sincronizar estos cambios (los del diagrama) con la base de datos generada. De acuerdo con lo anterior, puede revisar los siguientes pasos: 

    .row.justify-content-center.align-items-end.bg23
      .col-lg-6.my-4.j
        ul.lista-ul.fa-ul.mb-0.p-3                   
          li 
            i.fas.fa-code.color1
            | Esto se logra dando clic en Database > Synchronize Model.
          li 
            i.fas.fa-code.color1
            | Luego, seleccione la conexión local.
          li 
            i.fas.fa-code.color1
            | Luego, seleccione los datos en la parte de generación de script adicionales.
          li 
            i.fas.fa-code.color1
            | Después de pedir la contraseña se conecta; analice las bases de datos presentes y características del servidor.
          li 
            i.fas.fa-code.color1
            | Seleccione la base de datos con la que se va a sincronizar.
          li 
            i.fas.fa-code.color1
            | Analice las diferencias.
          li 
            i.fas.fa-code.color1
            | Al ubicarse en cada una de las entidades o tablas, se puede ignorar la actualización.
          li.mb-0 
            i.fas.fa-code.color1
            | En lugar de actualizar la base de datos, si lo que se quiere es actualizar el modelo (diagrama) para que quede conforme a la base de datos, se cliquea en el botón “Update Model”. Pero este no es el caso de interés porque se necesita actualizar la base de datos, entonces se da clic en Next.       

      .col-lg-6
        img.img-a.img-t.pt-5(data-aos="zoom-in")(src='@/assets/curso/temas/68.png', alt='')   

    p(data-aos="fade-down").mt-5 Al final del proceso se debe tener el DDL donde se genera la base datos y el DDL donde se actualiza la tabla factura. 

    Separador 
    #t_2_5.titulo-segundo.color-acento-contenido(data-aos="zoom-in-left")
      h2 2.5 Actualización por interfaz de línea de comandos 

    .row.justify-content-center.mb-5 
      .col-lg-3.my-3
        img.img-t.img-a(data-aos="zoom-in")(src='@/assets/curso/temas/70.png', alt='')            
      .col-lg-9.my-3
        p(data-aos="fade-down") Muchas veces no es el computador local el que interesa actualizar, sino más bien, un servidor en la nube. Algunas plataformas tienen un entorno gráfico que permite aplicar el script con unos cuantos clics desde una interfaz web, pero la mayoría ofrece una interfaz de consola o terminal, de manera que los recursos computacionales no se desperdician en interfaces gráficas.  

        h5.t1(data-aos="fade-down") Verifique los siguientes archivos:
        .row.justify-content-center.mb-5 
          .col.my-3
            a.anexo.mb-4(:href="obtenerLink('/downloads/DDL_drogueria.sql')" target="_blank")
              .anexo__icono
                img(src="@/assets/template/icono-doc.svg")
              .anexo__texto
                p #[b Anexo.] DDL_drogueria.sql
          .col.my-3
            a.anexo.mb-4(:href="obtenerLink('/downloads/DDL_update.sql')" target="_blank")
              .anexo__icono
                img(src="@/assets/template/icono-doc.svg")
              .anexo__texto
                p #[b Anexo.] DDL_update.sql
          .col.my-3
            a.anexo.mb-4(:href="obtenerLink('/downloads/ModeloFacturacionDrogueria.mwb')" target="_blank")
              .anexo__icono
                img(src="@/assets/template/icono-doc.svg")
              .anexo__texto
                p #[b Anexo.] ModeloFacturaciónDrogueria.mwb      

    .row.bg24.align-items-center.mb-5(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12  
            p(data-aos="fade-down").mb-5 #[b.t1 A continuación, se muestra cómo aplicar el script desde una terminal.] Esta base de datos se encuentra diseñada para cumplir el requerimiento funcional de administración de facturas de una droguería:

            .tarjeta.tarjeta--gris.p-4.mb-5(data-aos="fade-left")
              SlyderA(tipo="b")
                .row.justify-content-center.p-2
                  .col-lg-5.my-3.col-md-auto
                    h5 #[mark.bgtg.brad2.px-2 Paso 1]
                    .t5.pe-5
                      p Dar clic en el menú inicio, buscar MySQL, una terminal o interface de línea de comandados (Command Line Interface, CLI).   
                  .col-lg-5.my-3.mb-4.mb-md-0
                    img.img-a.img-t(src='@/assets/curso/temas/72.png', alt="")      

                .row.justify-content-center.p-2
                  .col-lg-5.my-3.col-md-auto
                    h5 #[mark.bgtg.brad2.px-2 Paso 2]
                    .t5.pe-5
                      p A continuación, pedirá la contraseña de root.   
                  .col-lg-5.my-3.mb-4.mb-md-0
                    img.img-a.img-t(src='@/assets/curso/temas/73.png', alt="")  

                .row.justify-content-center.p-2
                  .col-lg-5.my-3.col-md-auto
                    h5 #[mark.bgtg.brad2.px-2 Paso 3]
                    .t5.pe-5
                      p Luego, se debe seleccionar la base de datos con la sentencia SQL: use farmacia.  
                  .col-lg-5.my-3.mb-4.mb-md-0
                    img.img-a.img-t(src='@/assets/curso/temas/74.png', alt="")

    .row.justify-content-center.align-items-center          
      .col-lg-7.my-3
        .bg5.brad.px-3.mb-3
          .row.justify-content-center.align-items-center(data-aos="flip-down")           
            .col-lg-auto.my-3
              img.img-a.img-t(src='@/assets/curso/temas/76.png', alt='')       
            .col.my-3
              p(data-aos="fade-down").mb-0 A continuación, se describe un problema del cual se pretende obtener un modelo de datos que permita gestionar la información, a través de un sistema gestor de base de datos, como se realizó en el caso anterior, donde se fue empleando una estrategia empírica, luego de conocer los conceptos de bases de datos. 

        p(data-aos="fade-down") Se presentará un problema más sencillo con el ánimo de concentrar esfuerzos en el análisis desde un enfoque metodológico, que se puede basar en tres fases:                   
      .col-lg-5.my-3
        img.img-a.img-t(src='@/assets/curso/temas/75.png', alt='')       

    .row.justify-content-center.mb-4
      .col-lg-3.my-3.mov
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/77.png', alt='')      
      .col-lg-9.my-3(data-aos="fade-left")
        AcordionA(tipo="a" clase-tarjeta="tarjeta bg7")
          div(titulo="Diseño conceptual")
            p Encargado de entender el problema y la naturaleza de los datos (qué son y qué representan en el mundo real). Las actividades a desarrollar, son:
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Identificar entidades.
              li 
                i.fas.fa-code.color1
                | Identificar atributos.
              li 
                i.fas.fa-code.color1
                | Identificar las relaciones.
              li 
                i.fas.fa-code.color1
                | Identificar las cardinalidades de las relaciones.
              li 
                i.fas.fa-code.color1
                | Diagrama entidad relación.              
          div(titulo="Diseño lógico")
            p Se encarga de analizar la estructura de los datos y que se cumpla con los requisitos del negocio, modelo de negocio o problema. Las actividades a desarrollar, son:
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Mapear diagrama entidad relación a un modelo relacional.
              li 
                i.fas.fa-code.color1
                | Análisis de restricciones de integridad.
              li 
                i.fas.fa-code.color1
                | Validación de requisitos funcionales.              
          div(titulo="Diseño físico")
            p Se preocupa por cómo se almacenarán los datos. Las actividades a desarrollar, son:
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Definición de tipos de datos.
              li 
                i.fas.fa-code.color1
                | Analizar las restricciones de llaves foráneas.
              li 
                i.fas.fa-code.color1
                | Definición de índices.  

    h5.t1(data-aos="fade-down") Estudiemos ahora el caso 2, gestión de matrículas.        
    .row.justify-content-center.align-items-center          
      .col-lg-7.my-3
        .bg9.brad.p-4.mb-3
          p(data-aos="fade-down").mb-0 Se necesita un sistema que permita controlar la matrículas de un instituto de formación técnica profesional; donde interesa la información pertinente de los estudiantes como son los datos personales y la edad; y de los profesores parte de los datos personales como la titulación profesional o técnica y el año de graduación.  
        p(data-aos="fade-down") Cada programa técnico se desarrolla por semestres y un semestre tiene varias materias, cada semestre un estudiante puede matricular máximo 7 materias, un profesor puede orientar varias materias y la misma materia puede ser dictada por varios profesores. 
      .col-lg-5.my-3
        img.img-a.img-t(src='@/assets/curso/temas/78.png', alt='')  

    .row.justify-content-center.mb-5(data-aos="flip-down")           
      .col-lg-auto.my-3
        img.img-a.img-t(src='@/assets/curso/temas/79.png', alt='')       
      .col.my-3
        p(data-aos="fade-down").mb-0 Un estudiante puede estudiar varios programas, aunque no a la vez, y el estudiante se inscribe a un programa y cada año puede cursar 2 semestres (de enero a junio período 1, y de julio a diciembre período 2), si registra por semestre una matrícula con las materias a cursar. Algunos programas duran 5, 6 o 7 semestres.

    .row.justify-content-start.mb-4 
      .col-auto(data-aos="flip-down")
        .list
          .list__item
            .list__item__icon
              img(src='@/assets/curso/temas/icon.svg', alt='')
          .list__txt.bgicon.p-0.px-4
            h3.mb-0 Diseño conceptual 

    p(data-aos="fade-down") Para la elaboración del modelo conceptual es fundamental identificar las entidades, luego los atributos de cada una de ellas, luego las relaciones entre entidades y, si se desea, #[b.t1 se elabora un diagrama de entidad relación como resultado del diseño conceptual:] 

    .row.justify-content-center.mb-4    
      .col-lg-9.my-3(data-aos="fade-left")
        AcordionA(tipo="a" clase-tarjeta="tarjeta bg7")
          div(titulo="Lista de entidades")
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Persona (estudiantes y profesores): existen personas estudiantes y personas profesores.
              li 
                i.fas.fa-code.color1
                | Programa: representa la carrera técnica.
              li 
                i.fas.fa-code.color1
                | Inscripción: de un estudiante a un programa.
              li 
                i.fas.fa-code.color1
                | Materia.
              li 
                i.fas.fa-code.color1
                | Matrícula: dura un semestre y puede contener máximo 7 materias.    

          div(titulo="Lista de atributos")
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Estudiante (nombre, apellidos, identificación, fecha_nacimiento, correo, teléfono, dirección).
              li 
                i.fas.fa-code.color1
                | Profesor (nombre, apellidos, identificación, correo, teléfono, dirección, titulación, fecha  de titulación).
              li 
                i.fas.fa-code.color1
                | Programa (nombre del programa, nivel, número de semestres).
              li 
                i.fas.fa-code.color1
                | Inscripción (fecha, fecha de graduación).
              li 
                i.fas.fa-code.color1
                | Materia (nombre de la materia y semestre).
              li 
                i.fas.fa-code.color1
                | Matrícula (año, período).

          div(titulo="Relaciones y cardinalidad")
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | El estudiante puede tener varias inscripciones, pero una inscripción por un solo estudiante.
              li 
                i.fas.fa-code.color1
                | Un profesor puede dictar varias materias y una materia ser dictada por varios profesores.
              li 
                i.fas.fa-code.color1
                | Una inscripción puede ser la relación entre un único estudiante y un único programa.
              li 
                i.fas.fa-code.color1
                | Una inscripción puede tener varias matrículas, pero una matrícula corresponde a una única inscripción.
              li 
                i.fas.fa-code.color1
                | Una matrícula se relaciona con varios estudiantes y un estudiante con varias matrículas.
              li 
                i.fas.fa-code.color1
                | Una matrícula puede tener más de una materia, y la misma materia puede estar relacionada con varias matrículas.                
      .col-lg-3.my-3.mov
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/80.png', alt='')     

    .titulo-sexto.color-acento-contenido
      h5 Figura 15.
      span Diagrama entidad relación
    .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
      img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/81.svg', alt='La imagen presenta el diagrama entidad relación del caso que se está estudiando.') 
    p(data-aos="fade-down").mb-5 Actualmente, algunos diseñadores de bases de datos no diseñan el modelo entidad relación, por lo general directamente diseñan el modelo lógico o diagrama relacional, en algunos casos se emplea el modelo que se denomina modelo conceptual, que es equivalente al modelo entidad relación, pero difiere en la notación del diagrama al hacerse más parecido al modelo relacional. #[b.t1 Por este mismo motivo es poco usado, porque supone hacer un nuevo paso o transformación del modelo conceptual a un modelo lógico, siendo este último el que en realidad puede convertirse en una base de datos.] 

    .row.justify-content-start.mb-4 
      .col-auto(data-aos="flip-down")
        .list
          .list__item
            .list__item__icon
              img(src='@/assets/curso/temas/icon.svg', alt='')
          .list__txt.bgicon.p-0.px-4
            h3.mb-0 Diseño lógico

    p(data-aos="fade-down") Una vez se tiene el modelo conceptual, se mapea el diagrama entidad relación o también llamado modelo conceptual a un modelo lógico, esto mediante las reglas de multiplicidad entre entidades (de uno a uno, de uno a muchos y de muchos a muchos).   

    .row.bg25.align-items-center.mb-5(data-aos="fade-left")
      .col-lg-12.col-12.px-lg-5.px-4 
        .row.justify-content-center.align-items-center          
          .col-lg-12 
            .titulo-sexto.color-acento-contenido
              h5 Figura 16.
              span Mapear diagrama entidad relación a un modelo relacional
            .bgfig.p-5.brad.mb-5(data-aos="zoom-in") 
              img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/83.png', alt='Imagen que presenta cómo mapear el diagrama entidad relación a un modelo relacional.') 
            p(data-aos="fade-down").mb-5 Puede verificar algunos modelos, pero es recomendable que lo cree de manera que ejercite lo hasta ahora visto.    

            .row.justify-content-center.align-items-center          
              .col-lg-8
                .tarjeta.bg3.p-3(data-aos="fade-left")
                  .row.justify-content-around.align-items-center
                    .col-3.col-sm-2.col-lg-auto
                      img.img-t(src="@/assets/curso/temas/8.svg")
                    .col
                      .row.justify-content-between.align-items-center
                        .col.mb-3.mb-sm-0
                          h4.t4.mb-1 Modelos.mwb 
                          p.text-white Lo invitamos a visitar el siguiente , archivo Modelos.mwb 
                        .col-sm-auto
                          a.boton.color-acento-botones.ts(:href="obtenerLink('/downloads/Modelos.mwb')" target="_blank")
                            span Descargar
                            i.fas.fa-file-download  

            h5(data-aos="fade-down").my-5 Ahora, analicemos los siguientes pasos:     

            PasosB.color-acento-contenido.bg26.p-3.brad.mb-5
              .row.justify-content-center.mb-4(titulo="Paso 1")
                .col-8.order-1.my-3
                  h5 #[mark.bgtg.px-2 Análisis de restricciones de integridad]
                  .text-white
                    p La entidad matrícula tiene relación con una inscripción, y esta a su vez con un estudiante y con el programa al que pertenece, también podría haberse realizado la matrícula con el programa y el estudiante, pero convenientemente, al relacionar matrícula con inscripción con menos datos, se está relacionando el programa y el estudiante de forma indirecta. 

                    p Las demás relaciones responden al proceso de análisis de mapeo, por lo que no se entrará en detalles. 
              
                .col-lg-auto.order-lg-2.my-3 
                  img.img-a.img-t(src='@/assets/curso/temas/85.png', alt='')

              .row.justify-content-center.mb-4(titulo="Paso 2")
                .col-8.order-1.my-3
                  h5 #[mark.bgtg.px-2 Validación de requisitos funcionales]
                  .text-white
                    p Para conocer si se cumplen los requisitos funcionales de lógica es importante prestar atención a los siguientes puntos: 
                  ul.lista-ul.fa-ul.mb-0                   
                    li 
                      i.fas.fa-code.color
                      span.text-white Revise por cada atributo si es conveniente que sea No Null (No null o NN), o si no nulo representa algo conceptualmente en el proceso.
                    li 
                      i.fas.fa-code.color
                      span.text-white Si un atributo o columna es Not Null, revise si es importante definir un valor por defecto según la lógica del problema.               
                .col-lg-auto.order-lg-2.my-3 
                  img.img-a.img-t(src='@/assets/curso/temas/86.png', alt='') 

    .row.justify-content-start.mb-4 
      .col-auto(data-aos="flip-down")
        .list
          .list__item
            .list__item__icon
              img(src='@/assets/curso/temas/icon.svg', alt='')
          .list__txt.bgicon.p-0.px-4
            h3.mb-0 Diseño físico

    p(data-aos="fade-down") Finalmente, se debe revisar cuidadosamente la naturaleza de los datos antes de generar el archivo, conocer los tipos de datos que soporta el SGDB y estar seguro de que están bien definidos (si pueden no ser nulos, la longitud máxima y mínima, etc.):

    .row.justify-content-center.mb-4
      .col-lg-3.my-3.mov
        img.img-a.img-t(data-aos="zoom-in")(src='@/assets/curso/temas/87.png', alt='')      
      .col-lg-9.my-3(data-aos="fade-left")
        AcordionA(tipo="a" clase-tarjeta="tarjeta bg7")
          div(titulo="Definición de tipos de datos")
            p Revise:  
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Que el valor (entero y flotante) corresponda a los valores que en un momento dado puede tener, por ejemplo, mire que las materias id_materia es tipo SMALLINT (lo que permitiría 32767 materias) mientras que en personas id_persona es tipo INT (lo que permitiría 2147483647 personas, es decir, el más del 30% de la población mundial).

              li 
                i.fas.fa-code.color1
                | Preste especial atención en las cadenas de texto, tamaño máximo y mínimo en longitud.     

          div(titulo="Analizar las restricciones")
            p Considere: 
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Este es el punto estratégico del modelo, revisar la no nulidad o nulidad de las llaves foráneas es de vital importancia, porque ello determina en gran porcentaje si su modelo cumple los requerimientos funcionales del sistema, por ejemplo, una inscripción debe tener relacionado un id_estudiante y un id_programa, porque la lógica de una inscripción es que un estudiante se matricula a un programa de formación, por lo tanto ni id_estudiante, ni id_programa deben ser Null, por lo tanto son atributo con restricción Not Null (NN). 

          div(titulo="Definición de índices")
            p Valide:

            p Cómo se usa MySQL Workbench, esta hace por el diseñador muchas cosas, una de ellas es identificar los índices; sin embargo, si en algún momento decide hacer la base de datos en esta herramienta, no cree índices en los siguientes casos:  
            ul.lista-ul.fa-ul.mb-0                   
              li 
                i.fas.fa-code.color1
                | Por cada llave foránea se crea un índice.
              li 
                i.fas.fa-code.color1
                | Si va a hacer consultas por rango de fechas, a las columnas por las que va a filtrar por rango de fechas, créeles un índice.
              li 
                i.fas.fa-code.color1
                | No es necesario crear índices para las llaves primarias, por defecto MySQL lo hace.  

    .row.justify-content-center.align-items-center.px-3.bg27.brad(data-aos="flip-down")           
      .col-lg-auto.beat.my-3
        img.img-a.img-t(src='@/assets/curso/temas/3.svg', alt='')       
      .col.my-3
        p(data-aos="fade-down").mb-0 Si algún día usa otro motor de base de datos como Oracle, Postgres o SQL Server, verifique manualmente la creación de índices, porque según la herramienta que esté usando, puede ayudarle a crearlos para las llaves foráneas o no.                  
</template>

<script>
export default {
  name: 'Tema2',
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
