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



