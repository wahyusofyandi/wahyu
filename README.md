<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Glucacare Bharata - Obat Herbal Diabetes</title>
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <style>
    .slider-wrapper {
      position: relative;
      overflow: hidden;
      border-radius: 1rem;
      box-shadow: 0 20px 20px rgba(0, 0, 0, 0.1);
    }

    .slider-container {
      display: flex;
      transition: transform 0.7s ease-in-out;
      width: 100%;
    }

    .slider-image {
      object-fit: contain;
      flex-shrink: 0;
      width: 100%;
      max-width: 100%;
      height: 400px;
      padding: 0.25rem;
    }

    .slider-controls {
      position: absolute;
      top: 50%;
      left: 0;
      right: 0;
      display: flex;
      justify-content: space-between;
      transform: translateY(-50%);
      padding: 0 1rem;
      z-index: 10;
    }

    .slider-button {
      background-color: rgba(0, 0, 0, 0.4);
      border: none;
      color: white;
      padding: 0.5rem 1rem;
      border-radius: 9999px;
      cursor: pointer;
      font-size: 1.5rem;
    }

    .floating-wa {
      position: fixed;
      bottom: 20px;
      right: 20px;
      z-index: 50;
      background-color: #25D366;
      padding: 12px;
      border-radius: 9999px;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
  </style>
  <script>
    let currentSlide = 0;
    function updateSlider(sliderId) {
      const slider = document.getElementById(sliderId);
      const slides = slider.children;
      const slideWidth = slides[0].clientWidth;
      slider.style.transform = `translateX(-${currentSlide * slideWidth}px)`;
    }

    function changeSlide(sliderId, delta) {
      const slider = document.getElementById(sliderId);
      const totalSlides = slider.children.length;
      currentSlide = (currentSlide + delta + totalSlides) % totalSlides;
      updateSlider(sliderId);
    }

    function submitTestimonial() {
      const name = document.getElementById('name').value;
      const message = document.getElementById('message').value;
      if (name && message) {
        const testimonialSection = document.getElementById('testimonial-list');
        const newTestimonial = document.createElement('blockquote');
        newTestimonial.className = 'border-l-4 border-green-600 pl-4 italic';
        newTestimonial.innerHTML = `"${message}" – <strong>${name}</strong>`;
        testimonialSection.prepend(newTestimonial);
        document.getElementById('name').value = '';
        document.getElementById('message').value = '';
      }
    }

    window.onload = function () {
      setTimeout(() => {
        document.getElementById('popup').classList.remove('hidden');
      }, 5000);
      startCountdown();
      updateSlider("slider");
      updateSlider("realTestiSlider");
    };

    function closePopup() {
      document.getElementById('popup').classList.add('hidden');
    }

    function startCountdown() {
      const countdownEl = document.getElementById("countdown");
      let time = 60 * 30;
      const timer = setInterval(() => {
        const minutes = Math.floor(time / 60);
        const seconds = time % 60;
        countdownEl.textContent = `${minutes}m ${seconds < 10 ? '0' + seconds : seconds}s`;
        time--;
        if (time < 0) clearInterval(timer);
      }, 1000);
    }
  </script>
</head>
<body class="bg-yellow-50 text-gray-800 font-sans">
<!-- Konten tetap sama, hanya kode style dan script yang diperbaiki untuk tampilan dan fungsi slider -->
</body>
</html>
