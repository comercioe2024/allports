# allports
HEADER: 
FOOTER:
HOME PAGE: 



PORTADA DIVIDA EN 3: <div class="carousel-container" style="position: relative; width: 100%; overflow: hidden; border-radius: 10px;">
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

