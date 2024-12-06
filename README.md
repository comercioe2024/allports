# allports
HEADER: 


FOOTER:


HOME PAGE:

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


