<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>E K S - Escuela de Fútbol</title>
  <style>
    * {margin:0;padding:0;box-sizing:border-box;}
    body {
      font-family:'Arial',sans-serif;
      background: linear-gradient(to bottom, #a8e6cf, #dcedc1);
      color:#004d40;
      overflow-x:hidden;
    }
    header {
      background: linear-gradient(90deg,#0288d1,#43a047);
      color:white;
      padding:30px 20px;
      text-align:center;
      position:relative;
    }
    .logo {font-size:3em;font-weight:bold;letter-spacing:5px;}
    header h1 {margin-top:10px;font-size:2em;}
    nav {background:#004d40;display:flex;justify-content:center;gap:25px;padding:15px 0;}
    nav a {color:white;text-decoration:none;font-weight:bold;transition:0.3s;}
    nav a:hover {color:#ffeb3b;}
    section {padding:60px 20px;text-align:center;position:relative;}
    .section-bg {position:absolute;top:0;left:0;width:100%;height:100%;z-index:-1;opacity:0.1;background-size:cover;background-position:center;}
    .about, .programs, .contact {
      background:rgba(255,255,255,0.8);
      margin:20px auto;
      border-radius:15px;
      max-width:900px;
      padding:30px;
      box-shadow:0 5px 15px rgba(0,0,0,0.2);
    }
    .programs img {
      width:120px;
      margin:15px;
      transition: transform 0.3s;
      cursor:pointer;
    }
    .programs img:hover {transform: scale(1.2) rotate(15deg);}
    footer {background:#004d40;color:white;text-align:center;padding:25px;}
    button {
      background:#0288d1;color:white;border:none;padding:12px 25px;border-radius:8px;font-size:1.1em;cursor:pointer;transition:0.3s;
    }
    button:hover {background:#0277bd;transform:scale(1.05);}
    .ball {position:absolute;width:50px;animation: floatBall 5s infinite ease-in-out alternate;}
    @keyframes floatBall {
      0% {transform: translateY(0) rotate(0deg);}
      50% {transform: translateY(-30px) rotate(180deg);}
      100% {transform: translateY(0) rotate(360deg);}
    }
  </style>
</head>
<body>

  <!-- Balones animados (usando Base64 para imagen inline) -->
  <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABvUlEQVRYR+2WP0hUYRSGv3uX5QKzv7A4VAh4qBqgQmiiC9IhCL7CyrJqpiiIh4iC6BQ9dJEbPpGp6mYgH3kKJQjhD97s9PXNzz+7/5p75fO+70+9/3fjEB1EFaJ4mL9qVdBRzjQDHkAZ0YRiJQbPgFG3CU/CIN9xJ28DkNgNJcHVqM8ZobV6BAoIgdBY4B0KdfXhJ4DRwA7QMxkIuJ1yAVvi4CEZs5/Ae1AXn2d0f5hPOGxABUjC3n2k0r2nCwK4qLE/gwRnCSueBvkAt8N60BeQkXQF+4FW64hVmPCrT0AzgGfAueOk/2ANeAUZcRrxHfMFvk6g9cA18CkPEP/mu3k+Y+6LqmrBjgTZnV9S5RvwA2fGqQH4EXxM2p24r7qgAd5wC1wDeQd+4g1HMrnMFbUBoRrTq4ibZpr9osZr+O+ED9NHxtIoD/BnYVVn8Mu7kqtIAfslQyD0xgX+omUMm0gD7j9DdHy3Z8D1FgAAAABJRU5ErkJggg==" class="ball" style="top:50px; left:10%;">
  <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABvUlEQVRYR+2WP0hUYRSGv3uX5QKzv7A4VAh4qBqgQmiiC9IhCL7CyrJqpiiIh4iC6BQ9dJEbPpGp6mYgH3kKJQjhD97s9PXNzz+7/5p75fO+70+9/3fjEB1EFaJ4mL9qVdBRzjQDHkAZ0YRiJQbPgFG3CU/CIN9xJ28DkNgNJcHVqM8ZobV6BAoIgdBY4B0KdfXhJ4DRwA7QMxkIuJ1yAVvi4CEZs5/Ae1AXn2d0f5hPOGxABUjC3n2k0r2nCwK4qLE/gwRnCSueBvkAt8N60BeQkXQF+4FW64hVmPCrT0AzgGfAueOk/2ANeAUZcRrxHfMFvk6g9cA18CkPEP/mu3k+Y+6LqmrBjgTZnV9S5RvwA2fGqQH4EXxM2p24r7qgAd5wC1wDeQd+4g1HMrnMFbUBoRrTq4ibZpr9osZr+O+ED9NHxtIoD/BnYVVn8Mu7kqtIAfslQyD0xgX+omUMm0gD7j9DdHy3Z8D1FgAAAABJRU5ErkJggg==" class="ball" style="top:120px; left:80%; animation-duration:6s;">

  <header>
    <div class="logo">E K S</div>
    <h1>Escuela de Fútbol para Niños</h1>
  </header>

  <nav>
    <a href="#about">Nosotros</a>
    <a href="#programs">Programas</a>
    <a href="#contact">Contacto</a>
  </nav>

  <section id="about" class="about">
    <div class="section-bg" style="background-image:url('data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxAQEBUQEBUVFRUVFRUVFRUVFRUVFRUXFRUWFhUVFRUYHSggGBolGxUVITEhJSkrLi4uFx8zODMsNygtLisBCgoKDg0OGxAQGy0lICUtLS0tLy0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLf/AABEIAJ8BPgMBIgACEQEDEQH/xAAcAAACAgMBAQAAAAAAAAAAAAAABQMGAAECBwj/xAA9EAABAwIEBAQDBQYEBwAAAAABAAIRAyEEEjFBBVFhBhMicYGRoQYUMkKxwRVC0fAVFiM0YnKSwfDxJFRz4f/EABkBAAMBAQEAAAAAAAAAAAAAAAABAgMEBf/EACIRAQEBAAMAAwACAwEAAAAAAAABEQISAyExBBNBUSJxIv/aAAwDAQACEQMRAD8A+S9p0G0E0gDT0lDTaDR00DQ6kB6QFJiDJpNNOpA0oANJGg0ANOpA0aDSkANJGg0ANOpA0aDSkANJKaSkgGk0aDQA0aDQ6kDSgA0aDQ6kDSgA0aDQ6kDSgA0aDSk0aDSkANOpA0aDSkANJKaSkgGk0aDQA0aDQ6kDSgA0aDQ6kDSgA0aDQ6kDSgA0aDSk0aDSkANOpA0aDSkANJKaSkgGk0aDQA0aDQ6kDSgA0aDQ6kDSgA0aDQ6kDSgA0aDSk0aDSkANOpA0aDSkANJKaSkgGk0aDQA0aDQ6kDSgA0aDQ6kDSgA0aDQ6kDSgA0aDSk0aDSkANOpA0aDSkANJKaSkgGk0aDQA0aDQ6kDSgA0aDQ6kDSgA0aDQ6kDSgA0aDSk0aDSkANOpA0aDSk//2Q==');"></div>
    <h2>Sobre Nosotros</h2>
    <p>En <strong>E K S</strong> enseñamos fútbol a niños de todas las edades, fomentando valores como trabajo en equipo, disciplina y diversión.</p>
  </section>

  <section id="programs" class="programs">
    <h2>Nuestros Programas</h2>
    <p>Ofrecemos entrenamientos adaptados para cada grupo de edad:</p>
    <div>
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABvUlEQVRYR+2WP0hUYRSGv3uX5QKzv7A4VAh4qBqgQmiiC9IhCL7CyrJqpiiIh4iC6BQ9dJEbPpGp6mYgH3kKJQjhD97s9PXNzz+7/5p75fO+70+9/3fjEB1EFaJ4mL9qVdBRzjQDHkAZ0YRiJQbPgFG3CU/CIN9xJ28DkNgNJcHVqM8ZobV6BAoIgdBY4B0KdfXhJ4DRwA7QMxkIuJ1yAVvi4CEZs5/Ae1AXn2d0f5hPOGxABUjC3n2k0r2nCwK4qLE/gwRnCSueBvkAt8N60BeQkXQF+4FW64hVmPCrT0AzgGfAueOk/2ANeAUZcRrxHfMFvk6g9cA18CkPEP/mu3k+Y+6LqmrBjgTZnV9S5RvwA2fGqQH4EXxM2p24r7qgAd5wC1wDeQd+4g1HMrnMFbUBoRrTq4ibZpr9osZr+O+ED9NHxtIoD/BnYVVn8Mu7kqtIAfslQyD0xgX+omUMm0gD7j9DdHy3Z8D1FgAAAABJRU5ErkJggg==" alt="Balón">
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABiElEQVRYR+2WP0sDQRSGv3uX5QKzv7A4VAsOqAioIhCuhKYoURKlEi6pLFSl9ghuJicK0gSgqQzDxQdjFzqMfs/sjO7+Z35nXv2cXx9n91+wq1SaTIiKaV1knUQSRnVJnqQAJM0y2UqDmmJpRFBJk5R1pAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAAmzTJZkoCZQkk0mUGok5RlJpAA//2Q==" alt="Portería">
      <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAYAAABzenr0AAABXklEQVRYR+2WP0pDQRSGv1fMZLZyogoiCpiIqRCrSoqRFK0pMKpEiqAIiS3u9tFDC+IF6ixNk0Rtz5p5nzm/33s/vf7S+Gx8bH1lbIYoNykIaSkDMLJp9pQAnSTNY0g5pSaQUkGU6CklpJpBJDlNpKSaQKQ5TaSmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kp5BJDlNpmkEkO02kqT//2Q==" alt="Campo">
    </div>
  </section>

  <section id="contact" class="contact">
    <h2>Contacto</h2>
    <p>Correo: <strong>contacto@eksfutbol.com</strong></p>
    <p>Teléfono: <strong>+34 600 123 456</strong></p>
    <button onclick="alert('Gracias por tu interés, te contactaremos pronto!')">Enviar Mensaje</button>
  </section>

  <footer>
    &copy; 2025 E K S - Escuela de Fútbol
  </footer>

</body>
</html>
