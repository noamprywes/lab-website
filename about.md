---
layout: default
title: Research
permalink: /research/
---

<style>
  .research-container {
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    gap: 20px;
  }

  .research-text {
    flex: 1;
    text-align: justify;
  }

  .research-images {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }

  .research-images img {
    width: 100%;
    height: auto;
    object-fit: contain;
  }

  @media (max-width: 768px) {
    .research-container {
      flex-direction: column;
    }
  }
</style>

<div class="research-container">
  <div class="research-text">
    <h2>About the Lab</h2>
    <p>
      Plants, algae and cyanobacteria remove ~150 billion tonnes of carbon from the atmosphere every year. One enzyme, rubisco, is solely responsible for the carboxylation chemistry that ultimately feeds nearly all of the life on our planet. This enzyme has been extensively studied for decades but has proven very difficult to engineer.
    </p>
    <p>
      In the Prywes lab we use new, high-throughput enzymology methods to map out the fitness landscape of rubisco in order to study its evolution and for engineering purposes. High-throughput DNA sequencing and machine learning are newly applicable to the study of this critical enzyme.
    </p>
    <p>
      Photosynthetic engineering is an emerging discipline that has the potential to contribute to efforts to reduce carbon dioxide levels in our atmosphere. If rubisco could be improved it would have substantial implications for future efforts to draw down atmospheric carbon as fossil fuels are replaced by alternative energy sources.
    </p>
  </div>
  <div class="research-images">
    <img src="/images/9rub_rotate.gif" alt="twirling rubisco">
    <img src="/images/landscapeGif.gif" alt="landscape">
    <img src="/images/leaf.png" alt="leaf">
  </div>
</div>
