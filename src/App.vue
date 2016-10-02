<template id="app">
<div id="app">
  <nav-bar></nav-bar>
  <welcome></welcome>
  <about></about>
  <academics></academics>
  <experience></experience>
  <projects></projects>
  <skills></skills>
  <contact></contact>
  <site-footer></site-footer>
</div>
</template>

<script>
import About from './components/About'
import Academics from './components/Academics'
import Contact from './components/Contact'
import Experience from './components/Experience'
import NavBar from './components/NavBar'
import Projects from './components/Projects'
import SiteFooter from './components/SiteFooter'
import Skills from './components/Skills'
import Welcome from './components/Welcome'

export default {
  components: {
    About,
    Academics,
    Contact,
    Experience,
    NavBar,
    Projects,
    SiteFooter,
    Skills,
    Welcome
  }
}
</script>

<style lang="sass">
@import './assets/css/normalize.min.css';
@import './assets/css/skeleton.min.css';
@import './assets/css/styles.scss';

body {
  background-color: $sugar-cane;
  color: $nile-blue;
  font-style: normal;
  font-weight: 400;
  position: relative;
}

h1 {
  font-family: Montserrat, sans-serif;
  text-align: center;
  font-weight: 500;
  &.hero-heading {
    font-size: 100px;
  }
}

h4 {
  font-size: 2rem;
}

h5 {
  font-size: 1.7rem;
}

a {
  color: $puerto-rico;
  transition: all 200ms ease;
}

::selection {
  text-shadow: none;
  background: rgba($puerto-rico, 0.25);
}

.no-margin {
  margin: 0;
}

.no-padding {
  padding: 0 !important;
}

.align-right {
  text-align: right;
}

.align-left {
  text-align: left;
}

/* Shared
–––––––––––––––––––––––––––––––––––––––––––––––––– */
.button {
  border-radius: 100px;
  margin-bottom: 0;
  &-standalone {
    margin: 0 1rem;
  }
  &-primary {
    background-color: $puerto-rico !important;
    border-color: $puerto-rico !important;
  }
}

/* Sections
–––––––––––––––––––––––––––––––––––––––––––––––––– */
section {
  padding: 8rem 0;
  text-align: center;
}

.section {
  &-even {
    background-color: rgba($puerto-rico, 0.5);
    background-position: center;
    background-repeat: no-repeat;
  }
  &-heading,
  &-description {
    margin-bottom: 1.2rem;
  }
}

/* Media Queries
–––––––––––––––––––––––––––––––––––––––––––––––––– */

/* Bigger than 550 */
@media (min-width: 550px) {
  .section {
    padding: 12rem 0 11rem;
  }
  .hero {
    padding-bottom: 12rem;
    text-align: left;
    height: 165px;
  }
  .hero-heading {
    font-size: 2.4rem;
  }
}

/* Bigger than 750 */
@media (min-width: 750px) {
  .hero {
    height: 190px;
  }
  .hero-heading {
    font-size: 2.6rem;
  }
  .section {
    padding: 14rem 0 15rem;
  }
  .hero {
    padding: 16rem 0 14rem;
  }
  .section-description {
    max-width: 60%;
    margin-left: auto;
    margin-right: auto;
  }
  .categories {
    padding: 15rem 0 8rem;
  }
}

/* Bigger than 1000 */
@media (min-width: 1000px) {
  .section {
    padding: 20rem 0 19rem;
  }
  .hero {
    padding: 22rem 0;
  }
  .hero-heading {
    font-size: 3.0rem;
  }
}
</style>
