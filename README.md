# allports
HEADER: 


FOOTER:


HOME PAGE:

BOTON WHATSAPP:

<!-- Botón de WhatsApp -->
<a href="https://wa.me/1234567890" target="_blank" class="whatsapp-button">
    <img src="https://upload.wikimedia.org/wikipedia/commons/6/6b/WhatsApp.svg" alt="WhatsApp" class="whatsapp-icon">
</a>

<!-- Estilo CSS para el botón flotante -->
<style>
    .whatsapp-button {
        position: fixed;
        bottom: 20px; /* Ubicación en la parte inferior de la página */
        right: 20px; /* Ubicación en el lado derecho de la página */
        background-color: #25d366;
        border-radius: 50%;
        padding: 15px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.2);
        z-index: 1000;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        transition: background-color 0.3s;
    }

    .whatsapp-button:hover {
        background-color: #128c7e; /* Cambio de color al pasar el mouse */
    }

    .whatsapp-icon {
        width: 50px;
        height: 50px;
    }
</style>






PORTADA DIVIDA EN 3:

<div class="carousel-container" style="position: relative; width: 100%; overflow: hidden; border-radius: 10px;">
    <div class="carousel-slides" style="display: flex; transition: transform 0.5s ease-in-out;">
        <!-- Slide 1 -->
        <a href="{{store url='products/tienda.html'}}" style="min-width: 100%; display: block;">
            <img src="https://i.imgur.com/XkNtWmA.png" alt="Banner 1" style="width: 100%; display: block;">
        </a>
        <!-- Slide 2 -->
        <a href="{{store url='categoria-2'}}" style="min-width: 100%; display: block;">
            <img src="https://i.imgur.com/f4BDLQR.jpeg" alt="Banner 2" style="width: 100%; display: block;">
        </a>
        <!-- Slide 3 -->
        <a href="{{store url='categoria-3'}}" style="min-width: 100%; display: block;">
            <img src="https://i.imgur.com/RTZoPZw.png" alt="Banner 3" style="width: 100%; display: block;">
        </a>
    </div>
</div>

<script>
    // Variables
    const slides = document.querySelector('.carousel-slides');
    const totalSlides = document.querySelectorAll('.carousel-slides a').length;
    let currentIndex = 0;

    // Función para avanzar al siguiente slide
    function nextSlide() {
        currentIndex = (currentIndex + 1) % totalSlides;
        slides.style.transform = `translateX(-${currentIndex * 100}%)`;
    }

    // Cambio automático cada 5 segundos
    setInterval(nextSlide, 5000);
</script>


CONTADOR DE TIEMPO:

<!-- Contador regresivo para Navidad -->
<div id="countdown" style="font-family: Arial, sans-serif; text-align: center; padding: 20px; background-color: #242d4a; color: #fff; border-radius: 10px;">
    <h2>¡Nueva colección Jordan Air!</h2>
    <div id="timer" style="font-size: 30px; font-weight: bold; display: flex; justify-content: center; gap: 10px;">
        <div id="days" style="padding: 10px; background-color: #fff; color: #004aad; border-radius: 5px;"></div>
        <div id="hours" style="padding: 10px; background-color: #fff; color: #004aad; border-radius: 5px;"></div>
        <div id="minutes" style="padding: 10px; background-color: #fff; color: #004aad; border-radius: 5px;"></div>
        <div id="seconds" style="padding: 10px; background-color: #fff; color: #004aad; border-radius: 5px;"></div>
    </div>
</div>

<!-- Estilos CSS para el contador -->
<style>
    #countdown h2 {
        font-size: 24px;
        margin-bottom: 10px;
    }

    #timer div {
        font-size: 24px;
        font-weight: bold;
        padding: 15px;
        border-radius: 5px;
        background-color: #fff;
        color: #004aad;
    }
    
    #timer div span {
        display: block;
        font-size: 16px;
        color: #333;
    }
</style>

<!-- JavaScript para el contador de Navidad -->
<script>
    // Fecha objetivo: Navidad (25 de diciembre)
    const christmasDate = new Date("Dec 25, 2024 00:00:00").getTime();

    // Actualiza el contador cada segundo
    const x = setInterval(function() {

        // Obtén la fecha y hora actuales
        const now = new Date().getTime();
        
        // Encuentra la distancia entre ahora y la fecha de Navidad
        const distance = christmasDate - now;
        
        // Calcula el tiempo restante
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        // Muestra el resultado en el HTML
        document.getElementById("days").innerHTML = `${days} <span>Días</span>`;
        document.getElementById("hours").innerHTML = `${hours} <span>Horas</span>`;
        document.getElementById("minutes").innerHTML = `${minutes} <span>Minutos</span>`;
        document.getElementById("seconds").innerHTML = `${seconds} <span>Segundos</span>`;

        // Si el contador llega a 0, muestra un mensaje
        if (distance < 0) {
            clearInterval(x);
            document.getElementById("countdown").innerHTML = "<h2>¡Nueva colección!</h2>";
        }
    }, 1000);
</script>

SECCION DE BUSCADOR POR MARCAS

<div class="brand-section">
    <span class="arrow" id="prev-arrow">&#8249;</span>
    <div class="brand-carousel" id="carousel">
        <a href="https://www.underarmour.com" target="_blank">
            <img src="https://i.imgur.com/n1ZAOu5.jpeg" alt="Under Armour">
        </a>
        <a href="http://20.9.128.208/products/adidas.html" target="_blank">
            <img src="https://i.imgur.com/yeT5z94.jpeg" alt="Adidas">
        </a>
        <a href="https://www.converse.com" target="_blank">
            <img src="https://i.imgur.com/wxuMTI9.jpeg" alt="Converse">
        </a>
        <a href="https://www.puma.com" target="_blank">
            <img src="https://i.imgur.com/o0rip8w.jpeg" alt="Puma">
        </a>
        <a href="http://20.9.128.208/products/nike.html" target="_blank">
            <img src="https://i.imgur.com/zAUa3JU.jpeg" alt="Nike">
        </a>
        <a href="https://www.vans.com" target="_blank">
            <img src="https://i.imgur.com/cJKRkZG.jpeg" alt="Vans">
        </a>
        <a href="https://www.newbalance.com" target="_blank">
            <img src="https://i.imgur.com/k2yAVjB.jpeg" alt="New Balance">
        </a>
        <a href="https://imgur.com/OCUs1Q7" target="_blank">
            <img src="https://i.imgur.com/OCUs1Q7.jpeg" alt="Fila">
        </a>
        <a href="https://imgur.com/Uc7ij7" target="_blank">
            <img src="https://i.imgur.com/Uc7ij7j.jpeg" alt="Wilson">
        </a>
        <a href="http://20.9.128.208/reebok.html" target="_blank">
            <img src="https://i.imgur.com/lsHNleN.jpeg" alt="Reebok">
        </a>
    </div>
    <span class="arrow" id="next-arrow">&#8250;</span>
</div>



SECCION DESTACADOS: 

<!DOCTYPE html> 
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Productos</title>
    <style>
        .product-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .product-item {
            width: 200px;
            text-align: center;
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            position: relative;
            transition: transform 0.2s;
        }

        .product-item:hover {
            transform: scale(1.05);
        }

        .product-item img {
            width: 100%;
            height: auto;
        }

        .product-item h3 {
            font-size: 18px;
            margin: 10px 0;
        }

        .product-item .product-price {
            font-size: 16px;
            color: #333;
            margin: 5px 0;
        }

        .product-item .free-shipping {
            background-color: #003366;
            color: #ffffff;
            font-size: 14px;
            padding: 5px;
            border-radius: 5px;
            margin: 10px auto;
            display: inline-block;
        }

        .product-item .brand-icon {
            position: absolute;
            top: 10px;
            right: 10px;
            width: 30px;
            height: 30px;
        }
    </style>
</head>
<body>
    <div class="product-grid">
        <!-- Gorra Nike -->
        <a href="http://agtiendas.store/gorra-nike-logo-pipa.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/cache/c41affb7fe0f63ffd37172f4caba23a0/w/h/whatsapp_image_2024-11-28_at_11.03.16_pm_1_.jpeg" alt="Gorra Nike">
           
            <h3>Gorra Nike</h3>
            <p class="product-price">$24.999</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

        <!-- Gorra Jordan -->
        <a href="http://agtiendas.store/gorra-jordan-pro.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/cache/c41affb7fe0f63ffd37172f4caba23a0/w/h/whatsapp_image_2024-11-28_at_8.49.13_pm.jpeg" alt="Gorra Jordan Pro">
            <h3>Gorra Jordan Pro</h3>
            <p class="product-price">$35.999</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

        <!-- Medias Nike -->
        <a href="http://agtiendas.store/medias-nike-negras.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/w/h/whatsapp_image_2024-11-26_at_7.36.45_pm.jpeg" alt="Medias Nike">
           
            <h3>Medias Nike</h3>
            <p class="product-price">$15.000</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

        <!-- Remera Reebok -->
        <a href="http://agtiendas.store/remera-rebook-essentials-hombre.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/cache/c41affb7fe0f63ffd37172f4caba23a0/w/h/whatsapp_image_2024-11-26_at_22.44.59.jpeg" alt="Remera Reebok"> 
            <h3>Remera Reebok</h3>
            <p class="product-price">$57.999</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

        <!-- Zapatillas Air Force -->
        <a href="zapatillas-nike-air-force-one-mujer.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/cache/c41affb7fe0f63ffd37172f4caba23a0/w/h/whatsapp_image_2024-11-28_at_10.43.12_pm_1.jpeg" alt="Zapatillas Air Force">
           
            <h3>Zapatillas Air Force</h3>
            <p class="product-price">$89.999</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

    </div>
</body>
</html>


SECCION ADIDAS: 

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Productos</title>
    <style>
        .product-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .product-item {
            width: 200px;
            text-align: center;
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .product-item:hover {
            transform: scale(1.05);
        }

        .product-item img {
            width: 100%;
            height: auto;
        }

        .product-item h3 {
            font-size: 18px;
            margin: 10px 0;
        }

        .product-item .product-price {
            font-size: 16px;
            color: #333;
            margin: 5px 0;
        }

        .product-item .free-shipping {
            background-color: #003366;
            color: #ffffff;
            font-size: 14px;
            padding: 5px;
            border-radius: 5px;
            margin: 10px auto;
            display: inline-block;
        }
    </style>
</head>
<body>
    <div class="product-grid">
        <!-- Zapatillas Adidas -->
        <a href="http://20.9.128.208/zapatillas-adidas-nino-a.html" class="product-item">
            <img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/41c6de7a10e54487913bad7101606f42_9366/360_SANDAL_I_Negro_GX0864_01_standard.jpg" alt="Producto 1">
            <h3>Zapatillas Adidas</h3>
            <p class="product-price">$100.000</p>
            <div class="free-shipping">Envío gratis</div>
        </a>
        
        <!-- Botella Adidas -->
        <a href="http://20.9.128.208/botella-celeste-adidas.html" class="product-item">
            <img src="https://http2.mlstatic.com/D_Q_NP_982045-MLU73605013646_122023-O.webp" alt="Producto 2">
            <h3>Botella Adidas</h3>
            <p class="product-price">$15.000</p>
            <div class="free-shipping">Envío gratis</div>
        </a>
        
        <!-- Remera Argentina -->
        <a href="http://20.9.128.208/remera-argentina-adidas.html" class="product-item">
            <img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/29825b2765df4f449134febbd28f4f66_9366/Camiseta_Alternativa_Argentina_24_Azul_IP8403_01_laydown.jpg" alt="Producto 3">
            <h3>Remera Argentina</h3>
            <p class="product-price">$89.000</p>
            <div class="free-shipping">Envío gratis</div>
        </a>

        <!-- Top Deportivo Adidas -->
        <a href="http://20.9.128.208/top-deportivo-adidas-mujer.html" class="product-item">
            <img src="https://assets.adidas.com/images/w_600,f_auto,q_auto/8c2b9bc187e7474f98c1ae8300d92e0a_9366/Top_Deportivo_Powerreact_Training_Techfit_Soporte_Medio_Negro_HN7273_01_laydown.jpg" alt="Producto 4">
            <h3>Top Deportivo Adidas</h3>
            <p class="product-price">$41.000</p>
            <div class="free-shipping">Envío gratis</div>
 </a>

        <!-- Sandalias Adidas -->
        <a href="http://agtiendas.store/sandalias-adidas-nino-a.html" class="product-item">
            <img src="http://agtiendas.store/media/catalog/product/cache/c41affb7fe0f63ffd37172f4caba23a0/s/i/sin_t_tulo_700_x_700_px_1_.png" alt="Producto 4">
            <h3>Sandalias Adidas</h3>
            <p class="product-price">$68.000</p>
            <div class="free-shipping">Envío gratis</div>
        </a>
    </div>
</body>
</html>












ZAPATILLAS ADIDAS COLORES :

<!DOCTYPE html>
<html lang="en">
<head>
    
   
<meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Productos</title>
    <style>
        .product-grid {
            disp

        .product-grid {
            d

        .product-grid {
         

        .product-grid {
     

        .product-grid {

      

    

 

        .product-grid {
            display: flex;
            gap: 20px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .product-item {
            width: 200px;
            text-align: center;
            border: 1px solid #ddd;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s;
        }

        .product-item:hover {
            transform: scale(1.05);
        }

        .product-item img {
            width: 100%;
            height: auto;
        }

        .product-item h3 {
            font-size: 18px;
            margin: 10px 0;
        }

        .product-item .product-price {
            font-size: 16px;
            color: #333;
            margin: 5px 0;
        }

        .product-item .free-shipping {
            background-color: #003366;
            color: #ffffff;
            font-size: 14px;
            padding: 5px;
            border-radius: 5px;
            margin: 10px auto;
            display: inline-block;
        }
    </style>

</head
</head>


<body>
    <div class="product-grid">
        
    

 
<!-- Zapatillas Superstar Clásica -->
        <a href="http://20.9.128.208/zapatillas-adidas-superstar-originals.html" class="product-item">
            <img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/7ed0855435194229a525aad6009a0497_9366/Zapatillas_Superstar_Blanco_EG4958_01_standard.jpg" alt="Superstar Clásica">
            
         

      

   
<h3>Superstar Clásica</h3>
            <p class="product-price">$179.999</p>
            
      

    

 
<div class="free-shipping">Envío gratis</div>
        
    

  
</a>
        
        
        
        <!

        
       

        
    

        
<!-- Zapatillas Superstar Verde -->
        
    

  
<a href="http://20.9.128.208/zapatillas-adidas-superstar-originals.html" class="product-item">
            
           

       

  
<img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/68984814016b41d88b1b1de7c16aa168_9366/Zapatillas_Superstar_Blanco_ID1374_01_standard.jpg" alt="Superstar Verde">
            <h3>Superstar Verde</h3>
            
           
<p class="product-price">$179.999</p>
            
           
<div class="free-shipping">Envío gratis</div>
        
       
</a>
        
        
        
<!-- Zapatillas Superstar Bordeaux -->
        
        
<a href="http://20.9.128.208/zapatillas-adidas-superstar-originals.html" class="product-item">
            
           

     
<img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/759b91dd7cae46c39dc1aeed00c40bf7_9366/Zapatillas_Superstar_Blanco_HP9845_01_standard.jpg" alt="Superstar Bordeaux">
            
       

   
<h3>Superstar Bordeaux</h3>
            
         

     
<p class="product-price">$179.999</p>
            
          

     
<div class="free-shipping">Envío gratis</div>
        
        </

   
</a>        

        

        <!


  
<!-- Zapatillas Superstar Amarilla -->
        
     
<a href="http://20.9.128.208/zapatillas-adidas-superstar-originals.html" class="product-item">
            
         

  
<img src="https://assets.adidas.com/images/h_840,f_auto,q_auto,fl_lossy,c_fill,g_auto/dab45852f08c4172be05ae310056a68c_9366/Zapatillas_Superstar_Blanco_GZ4741_01_standard.jpg" alt="Superstar Amarilla">
            
  
<h3>Superstar Amarilla</h3>
            <p class="product-price">$179.999</p>
            
            

           
<div class="free-shipping">Envío gratis</div>
        </a>
    </div>
</body>
</html>







TITULO ADIDAS: 

<div id="countdown" style="font-family: Arial, sans-serif; text-align: center; padding: 20px; background-color: #242d4a; color: #ffffff; border-radius: 10px;">
    <h2>Adidas Superstar Originals</h2>

</div>

<!-- Estilos CSS para el contador -->
<style>
    #countdown h2 {
        font-size: 24px;
        margin-bottom: 10px;
    }

    #timer div {
        font-size: 24px;
        font-weight: bold;
        padding: 15px;
        border-radius: 5px;
        background-color: #fff;
        color: #004aad;
    }
    
    #timer div span {
        display: block;
        font-size: 16px;
        color: #333;
    }
</style>

<!-- JavaScript para el contador de Navidad -->
<script>
    // Fecha objetivo: Navidad (25 de diciembre)
    const christmasDate = new Date("Dec 25, 2024 00:00:00").getTime();

    // Actualiza el contador cada segundo
    const x = setInterval(function() {

        // Obtén la fecha y hora actuales
        const now = new Date().getTime();
        
        // Encuentra la distancia entre ahora y la fecha de Navidad
        const distance = christmasDate - now;
        
        // Calcula el tiempo restante
        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        // Muestra el resultado en el HTML
        document.getElementById("days").innerHTML = `${days} <span>Días</span>`;
        document.getElementById("hours").innerHTML = `${hours} <span>Horas</span>`;
        document.getElementById("minutes").innerHTML = `${minutes} <span>Minutos</span>`;
        document.getElementById("seconds").innerHTML = `${seconds} <span>Segundos</span>`;

        // Si el contador llega a 0, muestra un mensaje
        if (distance < 0) {
            clearInterval(x);
            document.getElementById("countdown").innerHTML = "<h2>¡Nueva colección!</h2>";
        }
    }, 1000);
</script>








TESTIMONIOS: 

<div class="testimonial">
    <p>"¡Las zapatillas son increíbles!" - <strong>Juan Pérez</strong></p>
    <div class="stars">
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
    </div>
</div>

<div class="testimonial">
    <p>"Me encantan mis superstar. Son súper cómodas para usarlas todo el día y combinan con casi toda mi ropa." - <strong>Ana Gómez</strong></p>
    <div class="stars">
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
    </div>
</div>

<div class="testimonial">
    <p>"Las uso para complementar mis outfits y siempre recibo comentarios positivos.¡Recomiendo totalmente!" - <strong>Carlos Rodríguez</strong></p>
    <div class="stars">
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
        <span class="star">&#9733;</span>
    </div>
</div>

<!-- Estilo CSS para las estrellas -->
<style>
    .testimonial {
        font-family: Arial, sans-serif;
        background-color: #004aad;
        padding: 20px;
        margin: 20px 0;
        border-radius: 10px;
        box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.1);
    }

    .testimonial p {
        font-size: 16px;
        color: #fff;
    }

    .customer-name {
        font-weight: bold;
        color: #555;
    }

    .stars {
        color: #FFD700;  /* Color amarillo para las estrellas */
        font-size: 20px;
    }

    .star {
        margin-right: 2px; /* Espacio entre las estrellas */
    }
</style>



TARJETAS DE CRÉDITO:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Medios de Pago</title>
    <style>
        .credit-cards {
            display: flex;
            gap: 10px;
            justify-content: center;
            margin: 20px;
        }

        .credit-cards img {
            width: 50px; /* Tamaño más pequeño */
            height: auto;
        }
    </style>
</head>
<body>
    <div class="credit-cards">
        <img src="https://newsport.vtexassets.com/assets/vtex/assets-builder/newsport.theme/4.0.14/img/footer/visa___ebca95f156bd36dbc03625849cdc7e15.svg" alt="Visa">
        <img src="https://newsport.vtexassets.com/assets/vtex/assets-builder/newsport.theme/4.0.14/img/footer/mastercard___7f0b6e086dd0d6cf2a6406e4b128eedb.svg" alt="Mastercard">
        <img src="https://newsport.vtexassets.com/assets/vtex/assets-builder/newsport.theme/4.0.14/img/footer/american-express___5f158bd210a9b080d61251b5b5a5a814.svg" alt="Amex">
        <img src="https://newsport.vtexassets.com/assets/vtex/assets-builder/newsport.theme/4.0.14/img/footer/pago-facil___9e4fa5e4372e805a34c7b22e52f29598.svg" alt="Pago Fácil">
    </div>
</body>
</html>



NEWSLETTER: 

<div style="background-color: #242d4a; padding: 15px; display: flex; align-items: center; justify-content: center; color: white; font-size: 16px;">
    <span style="margin-right: 10px;">Suscribite para enterarte de nuevos ingresos.</span>
    <!-- Formulario de Mailchimp -->
    <form action="https://example.us5.list-manage.com/subscribe/post?u=your-unique-id&amp;id=your-list-id" method="post" target="_blank" novalidate>
        <input type="email" name="EMAIL" placeholder="Ingrese su email" style="padding: 10px; border-radius: 5px; border: none; width: 250px; margin-right: 10px;" required>
        <button type="submit" style="background-color: white; color: #003366; border: none; padding: 10px 15px; border-radius: 5px; cursor: pointer;">
            ➔
        </button>
    </form>
</div>

QUIENES SOMOS:

<div style="display: flex; flex-wrap: wrap; align-items: center; padding: 20px; background-color: #f9f9f9; border-radius: 10px; gap: 20px;">
    <div style="flex: 1; min-width: 300px;">
        <h2 style="font-size: 28px; color: #0074D9;">Bienvenidos a All Sports</h2>
        <p style="font-size: 16px; color: #555; line-height: 1.6;">
           En All Sports, creemos que el deporte es para todos. Nos especializamos en ofrecer una amplia variedad de indumentaria, accesorios y calzados deportivos de alta calidad para hombres, mujeres y niños. 

Nuestro objetivo es acompañarte en cada paso de tu camino hacia el éxito, brindándote productos que te ayuden a alcanzar tus metas mientras luces increíble. 
        </p>
    </div>
    <div style="flex: 1; min-width: 300px; text-align: center;">
        <img src="{{media url='wysiwyg/freepik__candid-image-photography-natural-textures-highly-r__12445.jpeg}}" alt="All Sport" style="width: 100%; border-radius: 10px; box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);">
    </div>
</div>

<div style="padding: 20px; text-align: center; background-color: #0074D9; color: #fff; border-radius: 10px;">
    <h2 style="font-size: 28px; margin-bottom: 10px;">¡Empieza tu próxima aventura deportiva!</h2>
    <p style="font-size: 16px; margin-bottom: 20px;">Equípate con lo mejor en indumentaria deportiva. Descubre nuestra colección hoy mismo.</p>
    <a href="{{store url='products/tienda.html'}}" style="padding: 10px 20px; background-color: #fff; color: #0074D9; text-decoration: none; border-radius: 5px; font-size: 16px;">Explorar colecciones</a>
</div>
