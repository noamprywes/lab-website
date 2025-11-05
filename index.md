<a href="/about/">
  <picture id="main-photo-container">
    <source 
      id="mobile-photo-src"
      media="(max-width: 600px)" 
      srcset="/images/mainPagePhotos/mobile/mainPhoto1.jpg">
    <img 
      id="main-photo"
      src="/images/mainPagePhotos/mainPhoto1.jpg" 
      alt="Main photo" 
      style="width: 80%; max-width: 600px; height: auto; display: block; margin: 0 auto; border-radius: 8px; opacity: 0; transition: opacity 1s ease-in;">
  </picture>
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
  const totalPhotos = 27; // number of photos
  const randomIndex = Math.floor(Math.random() * totalPhotos) + 1;
  const imageFolder = "/images/mainPagePhotos/";
  const mobileFolder = "/images/mainPagePhotos/mobile/";
  
  const mainPhoto = document.getElementById("main-photo");
  const mobileSource = document.getElementById("mobile-photo-src");

  const chosenDesktop = `${imageFolder}mainPhoto${randomIndex}.jpg`;
  const chosenMobile = `${mobileFolder}mainPhoto${randomIndex}.jpg`;

  const img = new Image();
  img.src = chosenDesktop;
  img.onload = function() {
    mainPhoto.src = chosenDesktop;
    mobileSource.srcset = chosenMobile; // smaller image for mobile
    mainPhoto.style.opacity = 1;
  };
</script>

