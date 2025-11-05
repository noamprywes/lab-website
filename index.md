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
      class="logo-img dept-logo">
  </a>
  <img 
    src="/images/CambridgeLogo.jpg" 
    alt="University of Cambridge" 
    class="logo-img cam-logo">
</div>

<style>
  .logo-container {
    display: flex;
    justify-content: center; /* center them horizontally on desktop */
    align-items: center;
    width: 80%;
    max-width: 600px;
    margin: 40px auto 0 auto;
    gap: 24px; /* a bit more space between logos */
  }

  .logo-img {
    height: 60px;
    width: auto;
    object-fit: contain;
  }

  /* Make the department logo a bit larger for balance */
  .dept-logo {
    height: 70px;
  }

  /* Mobile view */
  @media (max-width: 600px) {
    .logo-container {
      flex-direction: column;
      justify-content: center; /* center on mobile */
      align-items: center;     /* change to flex-start for left-align */
      gap: 12px;
    }

    .logo-img {
      height: 60px;
    }

    .dept-logo {
      height: 65px; /* slightly smaller on mobile */
    }
  }
</style>

<script>
  // Randomly pick one of the numbered photos
  const totalPhotos = 27; // update to however many you have
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
