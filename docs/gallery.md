---
title: "ROAM Media Gallery"
layout: single
permalink: /gallery/
---

<section class="roam-section roam-section--gallery-intro">
  <h2>Build photos, integration snapshots, and demo footage</h2>
  <p>
    This page highlights the ROAM robotic welding system as it moves from integration to full-cell operation.
  </p>
  <p><a class="btn btn--primary btn--large" href="{{ '/' | relative_url }}">Roam Senior Design Home</a></p>
</section>

<section class="roam-section">
  <div class="roam-gallery-grid">
    <figure class="roam-gallery-card">
      <button class="roam-gallery-zoom" type="button" aria-label="Open image: Initial Proof-of-Concept CAD Validation<">
        <img src="{{ '/Documentation/Images/CellAssemRev1.png' | relative_url }}" alt="Initial Proof-of-Concept CAD Validation<" loading="lazy">
      </button>
      <figcaption>Initial Proof-of-Concept CAD Validation</figcaption>
    </figure>

    <figure class="roam-gallery-card">
      <button class="roam-gallery-zoom" type="button" aria-label="Open image: First coupons to tool-in TCP speed and welder settings">
        <img src="{{ '/assets/images/gallery/IMG_5625.jpg' | relative_url }}" alt="First coupons to tool-in TCP speed and welder settings" loading="lazy">
      </button>
      <figcaption>First Coupons to Tool-in TCP Speed and Welder Settings</figcaption>
    </figure>

    <figure class="roam-gallery-card">
      <button class="roam-gallery-zoom" type="button" aria-label="Open image: First Successful Coupon Test">
        <img src="{{ '/assets/images/gallery/IMG_5621.JPG' | relative_url }}" alt="First Successful Coupon Test" loading="lazy">
      </button>
      <figcaption>First Successful Coupon Test</figcaption>
    </figure>

    <figure class="roam-gallery-card">
      <button class="roam-gallery-zoom" type="button" aria-label="Open image: Original Torch Neck Integration Attempt">
        <img src="{{ '/assets/images/gallery/oldNeck.png' | relative_url }}" alt="Original Torch Neck Integration Attempt" loading="lazy">
      </button>
      <figcaption>Original Torch Neck Integration Attempt</figcaption>
    </figure>
  </div>
</section>

<div class="roam-lightbox" id="roamLightbox" hidden>
  <button class="roam-lightbox__backdrop" type="button" aria-label="Close image viewer"></button>
  <figure class="roam-lightbox__figure" role="dialog" aria-modal="true" aria-label="Expanded gallery image">
    <button class="roam-lightbox__close" type="button" aria-label="Close image viewer">&times;</button>
    <img class="roam-lightbox__image" alt="" loading="eager">
    <figcaption class="roam-lightbox__caption"></figcaption>
  </figure>
</div>

<script>
  (function () {
    var lightbox = document.getElementById("roamLightbox");
    if (!lightbox) return;

    var lightboxImage = lightbox.querySelector(".roam-lightbox__image");
    var lightboxCaption = lightbox.querySelector(".roam-lightbox__caption");
    var closeButtons = lightbox.querySelectorAll(".roam-lightbox__close, .roam-lightbox__backdrop");
    var triggers = document.querySelectorAll(".roam-gallery-zoom");

    function openLightbox(image, caption) {
      lightboxImage.src = image.currentSrc || image.src;
      lightboxImage.alt = image.alt || "Expanded gallery image";
      lightboxCaption.innerHTML = caption || "";
      lightbox.hidden = false;
      document.body.classList.add("roam-lightbox-open");
    }

    function closeLightbox() {
      lightbox.hidden = true;
      lightboxImage.src = "";
      document.body.classList.remove("roam-lightbox-open");
    }

    for (var i = 0; i < triggers.length; i += 1) {
      triggers[i].addEventListener("click", function () {
        var image = this.querySelector("img");
        if (!image || image.naturalWidth === 0) return;

        var figure = this.closest("figure");
        var caption = figure ? figure.querySelector("figcaption") : null;
        openLightbox(image, caption ? caption.innerHTML : "");
      });
    }

    for (var j = 0; j < closeButtons.length; j += 1) {
      closeButtons[j].addEventListener("click", closeLightbox);
    }

    document.addEventListener("keydown", function (event) {
      if (event.key === "Escape" && !lightbox.hidden) {
        closeLightbox();
      }
    });
  })();
</script>
