<!-- Clickable main photo -->
<div style="text-align:center;">
  <a href="/about/" id="main-photo-link" style="display: inline-block;">
    <picture id="main-photo-container">
      <source 
        id="mobile-photo-src"
        media="(max-width: 600px)" 
        srcset="/images/mainPagePhotos/mobile/mainPhoto1.jpg">
      <img 
        id="main-photo"
        src="/images/mainPagePhotos/mainPhoto1.jpg" 
        alt="Main photo" 
        style="width: 95%; max-width: 600px; height: auto; border-radius: 8px; opacity: 0; transition: opacity 1s ease-in;">
    </picture>
  </a>
</div>

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
    justify-content: center;
    align-items: center;
    width: 80%;
    max-width: 600px;
    margin: 40px auto 0;
    gap: 24px;
  }

  .logo-img {
    height: 60px;
    width: auto;
    object-fit: contain;
  }

  .dept-logo {
    height: 70px;
  }

  @media (max-width: 600px) {
    .logo-container {
      flex-direction: column;
      justify-content: center; /* or flex-start for left-align */
      align-items: center;
      gap: 12px;
    }

    .logo-img {
      height: 60px;
    }

    .dept-logo {
      height: 65px;
    }
  }
</style>

<script>
  const totalPhotos = 27;
  const randomIndex = Math.floor(Math.random() * totalPhotos) + 1;
  const imageFolder = "/images/mainPagePhotos/desktop/";
  const mobileFolder = "/images/mainPagePhotos/mobile/";

  const mainPhoto = document.getElementById("main-photo");
  const mobileSource = document.getElementById("mobile-photo-src");

  const chosenDesktop = `${imageFolder}mainPhoto${randomIndex}.jpg`;
  const chosenMobile = `${mobileFolder}mainPhoto${randomIndex}.jpg`;

  // Load smaller image first for faster perceived load on mobile
  const img = new Image();
  img.src = window.innerWidth <= 600 ? chosenMobile : chosenDesktop;
  img.onload = () => {
    mainPhoto.src = chosenDesktop;
    mobileSource.srcset = chosenMobile;
    mainPhoto.style.opacity = 1;
  };
</script>
