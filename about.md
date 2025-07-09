---
layout: default
title: About
permalink: /about/
---

<style>
.about-row {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 20px;
  margin-bottom: 40px;
}

.about-text {
  flex: 1;
  text-align: justify;
}

.about-image {
  flex: 1;
}

.about-image img {
  max-width: 100%;
  height: auto;
}

@media (max-width: 768px) {
  .about-row {
    flex-direction: column;
  }
}
</style>

<h1>About the Lab</h1>

<div class="about-row">
  <div class="about-text">
    <p>
      Plants, algae and cyanobacteria remove ~150 billion tonnes of carbon from the atmosphere every year. One enzyme, rubisco, is solely responsible for the carboxylation chemistry that ultimately feeds nearly all of the life on our planet.
    </p>
  </div>
  <div class="about-image">
    <img src="/images/leaf.png" alt="Leaf illustration">
  </div>
</div>

<div class="about-row">
  <div class="about-text">
    <p>
      In the Prywes lab we use new, high-throughput enzymology methods to map out the fitness landscape of rubisco in order to study its evolution and for engineering purposes. High-throughput DNA sequencing and machine learning are newly applicable to the study of this critical enzyme.
    </p>
  </div>
  <div class="about-image">
    <img src="/images/landscapeGif.gif" alt="Landscape schematic">
  </div>
</div>

<div class="about-row">
  <div class="about-text">
    <p>
      Photosynthetic engineering is an emerging discipline that has the potential to contribute to efforts to reduce carbon dioxide levels in our atmosphere. If rubisco could be improved it would have substantial implications for future efforts to draw down atmospheric carbon as fossil fuels are replaced by alternative energy sources.
    </p>
  </div>
  <div class="about-image">
    <img src="/images/9rub_rotate.gif" alt="Rotating Rubisco animation">
  </div>
</div>
