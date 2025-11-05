<a href="/about/">
  <img 
    id="main-photo"
    src="/images/mainPagePhotos/mainPhoto1.jpg" 
    alt="Main photo" 
    style="width: 80%; max-width: 600px; height: auto; display: block; margin: 0 auto; border-radius: 8px; opacity: 0; transition: opacity 1s ease-in;">
</a>

<!-- Department and University Logos -->
<div class="logo-container">
  <a href="https://www.bioc.cam.ac.uk/" target="_blank" rel="noopener noreferrer">
    <img 
      src="/images/deptLogo.jpg" 
      alt="Department of Biochemistry, University of Cambridge" 
      class="logo-img">
  </a>
  <img 
    src="/images/CambridgeLogo.jpg" 
    alt="University of Cambridge" 
    class="logo-img">
</div>

<style>
  .logo-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 80%;
    max-width: 600px;
    margin: 40px auto 0 auto;
    gap: 16px;
  }

  .logo-img {
    width: 45%;
    height: auto;
    max-height: 60px;
    object-fit: contain;
  }

  @media (max-width: 600px) {
    .logo-container {
      flex-direction: column;
      align-items: center;
    }

    .logo-img {
      width: 60%;
      max-height: 60px;
    }
  }
</style>

<script>
  // Randomly pick one of the numbered photos
  const totalPhotos = 27; // ← set this to however many you have
  const randomIndex = Math.floor(Math.random() * totalPhotos) + 1;
  const imageFolder = "/images/mainPagePhotos/";
  const mainPhoto = document.getElementById("main-photo");

  const img = new Image();
  img.src = `${imageFolder}mainPhoto${randomIndex}.jpg`;

  img.onload = function() {
    mainPhoto.src = img.src;
    mainPhoto.style.opacity = 1;
  };
</script>
