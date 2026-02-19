---
title: "ROAM Robotic Welding Senior Design Project"
layout: splash
permalink: /
header:
  overlay_color: "#808080"
  overlay_filter: "0.5"
  overlay_image: "/Documentation/Images/CellAssemRev1.png"
  overlay_video: "/assets/videos/landing-hero.mp4"
  caption: "ROAM robotic welding cell - first running iteration"
  actions:
    - label: "Explore Repository"
      url: "https://github.com/Bgujer/ROAM-Robotic_Welding_Senior_Design"
      class: "btn btn--primary"
    - label: "View Media Gallery"
      url: "/gallery/"
      class: "btn btn--primary"
excerpt: "A CSU senior design robotic welding platform focused on safe, repeatable automation at a practical cost objective."
---

<section class="roam-section roam-section--objective">
  <p class="roam-kicker">Main Objective</p>
  <h2>Build a dependable robotic welding system for real lab use</h2>
  <p>
    The ROAM / Rapid Prototyping Lab (RPL) Robotic Welding Senior Design Project's (Fall 2025 - Spring 2026)
    spcope involved integrating a <strong>UFactory xArm 850</strong> with manual welding hardware.
    Our objective is to design a safe and repeatable weld execution while holding a
    project cost objective near <strong>$20,000</strong> to allow for an acessable price-point for our project's end user, ROAM Electric.
  </p>
</section>

<section class="roam-section">
  <p class="roam-kicker">System Snapshot</p>
  <div class="roam-grid roam-grid--two">
    <article class="roam-card">
      <h3>Platform</h3>
      <ul>
        <li><strong>Robot:</strong> UFactory xArm 850</li>
        <li><strong>Welder:</strong> Miller MillerMatic Pro</li>
        <li><strong>End Effector:</strong> Custom torch mount and adapter</li>
      </ul>
    </article>
    <article class="roam-card">
      <h3>Controls and Safety</h3>
      <ul>
        <li><strong>Control Stack:</strong> UFactory Studio, Python, ROS</li>
        <li><strong>Safety:</strong> Emergency Stop and Built-in Collision Detection via Torque Feedback </li>
      </ul>
    </article>
  </div>
</section>

<section class="roam-section">
  <p class="roam-kicker">Progress Highlights</p>
  <div class="roam-grid roam-grid--two">
    <article class="roam-card">
      <h3>Initiating Welds from Controler</h3>
      <p>Tied into the manual welder trigger and retrofitted it to actuate off of a signal sent from our controller.</p>
    </article>
    <article class="roam-card">
      <h3>Full Cell Design</h3>
      <p>Designed a cell to be an all-in-one system, allowing for easy moves across factory floors - simulating an end product similar to $100k+ turn-key systems.</p>
    </article>
  </div>
</section>

<section class="roam-section">
  <p class="roam-kicker">Meet the Team</p>
  <img class="roam-team-banner" src="{{ '/assets/images/DSC_1994%20(1).JPG' | relative_url }}" alt="ROAM senior design team photo" loading="lazy">
  <p class="roam-team-hint"><em>*Hover (or tap a card on mobile) for more details*</em></p>
  <div class="roam-grid roam-grid--team">
    <article class="roam-card roam-card--person" tabindex="0">
      <h3>Ben Gujer</h3>
      <p class="role">Controls Focus</p>
      <div class="roam-person-hover">
        <p>Welder integration and safety</p>
      </div>
    </article>
    <article class="roam-card roam-card--person" tabindex="0">
      <h3>Dexter Shafer-White</h3>
      <p class="role">Controls Focus</p>
      <div class="roam-person-hover">
        <p>xArm control scripts and path planning logic</p>
      </div>
    </article>
    <article class="roam-card roam-card--person" tabindex="0">
      <h3>Gage Steinke</h3>
      <p class="role">Mechanical Focus</p>
      <div class="roam-person-hover">
        <p>Welder interface and torch mounting system</p>
      </div>
    </article>
    <article class="roam-card roam-card--person" tabindex="0">
      <h3>Greg Hider</h3>
      <p class="role">Mechanical Focus</p>
      <div class="roam-person-hover">
        <p>Welder interface and supporting mounting systems</p>
      </div>
    </article>
    <article class="roam-card roam-card--person" tabindex="0">
      <h3>Tamsin Izard</h3>
      <p class="role">Project Manager</p>
      <div class="roam-person-hover">
        <p>Timeline, documentation, and meeting coordination</p>
      </div>
    </article>
  </div>
</section>

<section class="roam-section roam-section--note">
  <p><strong>Confidentiality note:</strong> Some project elements may be confidential under NDA. Do not upload or disclose ROAM confidential information without written permission.</p>
</section>

<script>
  (function () {
    var isTouchLike = window.matchMedia("(hover: none), (pointer: coarse)").matches;

    if (!isTouchLike) {
      return;
    }

    var cards = Array.prototype.slice.call(document.querySelectorAll('.roam-card--person'));

    if (!cards.length) {
      return;
    }

    function closeAll(exceptCard) {
      cards.forEach(function (card) {
        if (card !== exceptCard) {
          card.classList.remove('is-open');
          card.setAttribute('aria-expanded', 'false');
        }
      });
    }

    cards.forEach(function (card) {
      card.setAttribute('role', 'button');
      card.setAttribute('aria-expanded', 'false');

      card.addEventListener('click', function () {
        var willOpen = !card.classList.contains('is-open');
        closeAll(card);
        card.classList.toggle('is-open', willOpen);
        card.setAttribute('aria-expanded', willOpen ? 'true' : 'false');
      });

      card.addEventListener('keydown', function (event) {
        if (event.key === 'Enter' || event.key === ' ') {
          event.preventDefault();
          card.click();
        }
      });
    });

    document.addEventListener('click', function (event) {
      var clickedCard = event.target.closest('.roam-card--person');
      if (!clickedCard) {
        closeAll();
      }
    });
  })();
</script>
