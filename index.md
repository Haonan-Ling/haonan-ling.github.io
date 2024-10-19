---
---

The Ling lab aims at exploring the light-matter interactions in nanoscale electronic and photonic devices and newly emerging materials for further advancing the semiconductor technology. **We are actively expanding and are currently looking for PhD, Master, and undergraduate students to join our team!** Please see [here](team) for more information.

# My Image Slider

<div class="slider">
  <div class="slides">
    <img src="images/homeslider/2D_Materials.png" alt="Image 1">
    <img src="images/homeslider/Fume Hood.png" alt="Image 2">
    <img src="images/homeslider/Transfer Stage.png" alt="Image 3">
  </div>
  
  <button class="prev" onclick="plusSlides(-1)">&#10094;</button>
  <button class="next" onclick="plusSlides(1)">&#10095;</button>
</div>

<style>
  .slider {
    position: relative;
    max-width: 100%;
    margin: auto;
  }
  
  .slides img {
    width: 100%;
    display: none;
  }

  .prev, .next {
    cursor: pointer;
    position: absolute;
    top: 50%;
    width: auto;
    padding: 16px;
    margin-top: -22px;
    color: white;
    font-weight: bold;
    font-size: 18px;
    transition: 0.6s ease;
    border-radius: 0 3px 3px 0;
    user-select: none;
  }

  .prev {
    left: 0;
    border-radius: 3px 0 0 3px;
  }

  .next {
    right: 0;
    border-radius: 0 3px 3px 0;
  }
</style>

<script>
  let slideIndex = 1;
  showSlides(slideIndex);

  function plusSlides(n) {
    showSlides(slideIndex += n);
  }

  function showSlides(n) {
    let i;
    let slides = document.querySelectorAll(".slides img");
    if (n > slides.length) { slideIndex = 1 }
    if (n < 1) { slideIndex = slides.length }
    for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
    }
    slides[slideIndex - 1].style.display = "block";
  }
</script>

We are a new, growing research group residing in the [Mechanical and Aerospace Engineering Department](https://mae.ucf.edu/) at UCF. There are two major research thrusts in our lab:
* Design, fabrication, and characterization of electronic and photonic devices based on novel material systems, including low dimensional materials, phase change materials, superlattice structures, with improved capabilities
* Understanding the energy transfer mechanism in newly emerging material platforms such as layered van der Waals materials via optical spectroscopic and microscopic techniques

<!-- end of the list -->

Please see [Research](research) for more details. 
