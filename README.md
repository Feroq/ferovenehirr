<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Ferovenehir - Aşkımızın Hikayesi</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Dancing+Script&family=Open+Sans&display=swap');

  body {
    margin: 0;
    background: linear-gradient(135deg, #fceabb, #f8b500);
    font-family: 'Open Sans', sans-serif;
    color: #4a2c2a;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px 10px 50px;
  }
  header {
    font-family: 'Dancing Script', cursive;
    font-size: 3rem;
    margin-bottom: 20px;
    text-shadow: 2px 2px 6px #b37400;
  }
  main {
    width: 100%;
    max-width: 600px;
    background: #fff8f2;
    border-radius: 15px;
    padding: 30px 25px 40px;
    box-shadow: 0 10px 25px rgba(255, 105, 135, 0.35);
    text-align: center;
  }
  .poem {
    font-family: 'Dancing Script', cursive;
    font-size: 1.8rem;
    line-height: 1.6;
    margin-bottom: 35px;
    color: #6b3a3a;
  }
  .gallery {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
    margin-bottom: 35px;
  }
  .gallery img {
    width: 100%;
    border-radius: 15px;
    cursor: pointer;
    box-shadow: 0 6px 18px rgba(255,105,135,0.25);
    transition: transform 0.3s ease;
  }
  .gallery img:hover {
    transform: scale(1.05);
  }
  .music {
    margin-top: 10px;
  }

  /* Modal ışık kutusu */
  .modal {
    display: none;
    position: fixed;
    z-index: 10;
    padding-top: 60px;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    background-color: rgba(0,0,0,0.85);
  }
  .modal-content {
    margin: auto;
    display: block;
    max-width: 90%;
    max-height: 80%;
    border-radius: 15px;
  }
  .close {
    position: fixed;
    top: 25px;
    right: 30px;
    color: #fff;
    font-size: 38px;
    font-weight: bold;
    cursor: pointer;
    user-select: none;
  }
</style>
</head>
<body>

<header>Ferovenehir</header>

<main>
  <section class="poem">
    <p>
      Kalplerimiz birleşti, <br />
      Aşkımız her daim taze.<br />
      Seninle hayat bir şiir,<br />
      Sevgiyle dolu her an.
    </p>
  </section>

  <section class="gallery">
    <img src="https://i.ibb.co/4Vtb9Ln/fero-1.jpg" alt="Fotoğraf 1" onclick="openModal(this.src)" />
    <img src="https://i.ibb.co/4Vtb9Ln/fero-1.jpg" alt="Fotoğraf 1 Tekrar" onclick="openModal(this.src)" />
    <img src="https://i.ibb.co/Yj6jFxC/fero-3.jpg" alt="Fotoğraf 3" onclick="openModal(this.src)" />
    <img src="https://i.ibb.co/Yj6jFxC/fero-3.jpg" alt="Fotoğraf 3 Tekrar" onclick="openModal(this.src)" />
  </section>

  <section class="music">
    <iframe width="100%" height="180" src="https://www.youtube.com/embed/fKwr3i2iQQI?autoplay=0&loop=1&playlist=fKwr3i2iQQI" 
    frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
  </section>
</main>

<!-- Modal -->
<div id="modal" class="modal" onclick="closeModal()">
  <span class="close" onclick="closeModal(event)">&times;</span>
  <img class="modal-content" id="modal-img" />
</div>

<script>
  function openModal(src) {
    document.getElementById('modal-img').src = src;
    document.getElementById('modal').style.display = "block";
  }
  function closeModal(event) {
    if(event) event.stopPropagation();
    document.getElementById('modal').style.display = "none";
  }
</script>

</body>
</html>
