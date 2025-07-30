# aditya_gallery
A static image gallery website named Aditya Gallery – inspired by GeekyGallery.in – showcasing posters across categories like Anime, Movies, Sports, and Motivation. No pricing or ordering, just a clean gallery to view.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Aditya Gallery</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f3f3f3;
    }
    header {
      background: #111;
      color: #fff;
      padding: 1rem;
      text-align: center;
      font-size: 1.8rem;
      font-weight: bold;
    }
    nav {
      display: flex;
      justify-content: center;
      gap: 1rem;
      background: #222;
      padding: 0.5rem;
    }
    nav a {
      color: white;
      text-decoration: none;
      font-weight: bold;
    }
    .section-title {
      text-align: center;
      font-size: 1.5rem;
      margin-top: 2rem;
    }
    .gallery {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 1rem;
      padding: 1rem;
    }
    .gallery img {
      width: 100%;
      border-radius: 8px;
      cursor: pointer;
      transition: transform 0.3s ease;
    }
    .gallery img:hover {
      transform: scale(1.05);
    }
    footer {
      background: #111;
      color: white;
      text-align: center;
      padding: 1rem;
      margin-top: 2rem;
    }
    /* Lightbox */
    #lightbox {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.8);
      display: none;
      justify-content: center;
      align-items: center;
    }
    #lightbox img {
      max-width: 90%;
      max-height: 90%;
      border-radius: 10px;
    }
  </style>
</head>
<body>
  <header>Aditya Gallery</header>
  <nav>
    <a href="#anime">Anime</a>
    <a href="#movies">Movies</a>
    <a href="#sports">Sports</a>
    <a href="#motivation">Motivation</a>
  </nav>

  <div id="lightbox" onclick="this.style.display='none'">
    <img id="lightbox-img" src="">
  </div>

  <section id="anime">
    <h2 class="section-title">Anime Posters</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/300x400?text=Anime+1" alt="Anime 1" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Anime+2" alt="Anime 2" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Anime+3" alt="Anime 3" onclick="openLightbox(this.src)">
    </div>
  </section>

  <section id="movies">
    <h2 class="section-title">Movie Posters</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/300x400?text=Movie+1" alt="Movie 1" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Movie+2" alt="Movie 2" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Movie+3" alt="Movie 3" onclick="openLightbox(this.src)">
    </div>
  </section>

  <section id="sports">
    <h2 class="section-title">Sports Posters</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/300x400?text=Sports+1" alt="Sports 1" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Sports+2" alt="Sports 2" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Sports+3" alt="Sports 3" onclick="openLightbox(this.src)">
    </div>
  </section>

  <section id="motivation">
    <h2 class="section-title">Motivational Posters</h2>
    <div class="gallery">
      <img src="https://via.placeholder.com/300x400?text=Motivation+1" alt="Motivation 1" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Motivation+2" alt="Motivation 2" onclick="openLightbox(this.src)">
      <img src="https://via.placeholder.com/300x400?text=Motivation+3" alt="Motivation 3" onclick="openLightbox(this.src)">
    </div>
  </section>

  <footer>&copy; 2025 Aditya Gallery. All rights reserved.</footer>

  <script>
    function openLightbox(src) {
      document.getElementById('lightbox-img').src = src;
      document.getElementById('lightbox').style.display = 'flex';
    }
  </script>
</body>
</html>
