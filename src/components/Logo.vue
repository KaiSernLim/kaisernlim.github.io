<template>
<li id="logo">
  <a href="#about">
    <svg class="logo" viewBox="0 0 740 740">
    <circle class="a" cx="370" cy="370" r="350"/>
      <path class="b preload" d="M620.77,129.94L125.23,624.31A348.93,348.93,0,0,0,374.76,728.89c193.3,0,350-156.7,350-350A348.92,348.92,0,0,0,620.77,129.94Z" transform="translate(-4.76 -7.6)"/>
      <circle class="c" cx="370" cy="369" r="279.53"/>
      <path class="d preload" d="M575.06,176.64a278.59,278.59,0,0,1,79.23,194.95c0,154.38-125.15,279.53-279.53,279.53a278.58,278.58,0,0,1-193.58-77.89Z" transform="translate(-4.76 -7.6)"/>
      <line class="e" x1="66.23" y1="210.1" x2="351.26" y2="210.1"/>
      <line class="e" x1="406.35" y1="216.58" x2="678.05" y2="216.58"/>
      <line class="e" x1="265.72" y1="46.85" x2="265.72" y2="695.73"/>
      <polyline class="e" points="56.92 526.63 265.72 210.1 352.32 385.71"/>
      <line class="e" x1="489.1" y1="46.85" x2="489.1" y2="681.14"/>
      <polyline class="e" points="362.27 539.28 489.1 216.58 679.23 526.63"/>
      <circle class="e" cx="370" cy="370" r="350"/>
      <circle class="e" cx="370.97" cy="367.7" r="265.97"/>
    </svg>
  </a>
</li>
</template>

<script>
import $ from 'jquery'

$(document).ready(function () {
  $('.logo').hover(() => $('.b, .d').removeClass('preload'))
})
</script>

<style lang="sass">
/* Sass Variables
–––––––––––––––––––––––––––––––––––––––––––––––––– */
$logo-size: 50px;

/* Mixins
–––––––––––––––––––––––––––––––––––––––––––––––––– */
@mixin applyInfinite ($name, $duration, $style) {
  -webkit-animation: $name $duration $style infinite;
  -moz-animation: $name $duration $style infinite;
  animation: $name $duration $style infinite;
}

@mixin applyFinite ($name, $duration, $style) {
  -webkit-animation: $name $duration $style;
  -moz-animation: $name $duration $style;
  animation: $name $duration $style;
}

/* Animations
–––––––––––––––––––––––––––––––––––––––––––––––––– */
@keyframes spinOut400 {
  from { transform: rotate(400deg); }
  to { transform: rotate(0deg); }
}

@keyframes spinOut300 {
  from { transform: rotate(300deg); }
  to { transform: rotate(0deg); }
}

@keyframes spinAround {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

// Disable page load animation
.preload {
  -webkit-animation: none !important;
  -moz-animation: none !important;
  animation: none !important;
}

// Fix rotation center
.b, .d {
  transform-origin: 40% 40%;
  display: inline-block;
}

// Apply rotations
.b {
  @include applyFinite(spinOut300, 0.3s, linear)
}

.d {
  @include applyFinite(spinOut400, 0.3s, linear)
}

.a {
  fill:#4ecdc4;
}

.b {
  fill:#ffe66d;
}

.c {
  fill:#f7fff7;
}

.d {
  fill:#ff6b6b;
}

.e {
  fill:none;stroke:#1a535c;
  stroke-linecap:round;
  stroke-miterlimit:10;
  stroke-width:40px;
}

.logo {
  width: $logo-size;
  height: $logo-size;
  padding: 0 !important;
  &:hover {
    .b {
      @include applyInfinite(spinAround, 1.3s, ease)
    }

    .d {
      @include applyInfinite(spinAround, 0.9s, ease)
    }
  }
}

/* Styling
–––––––––––––––––––––––––––––––––––––––––––––––––– */
#logo {
  float: left;
  width: $logo-size;
  height: $logo-size;
  margin: 1rem 0;

  & > a {
    width: $logo-size;
    height: $logo-size;
    padding: 0 !important;
  }
}
</style>
