<template id="app">
  <div id="app">
    <nav-bar></nav-bar>
    <welcome></welcome>
    <about></about>
    <academics></academics>
    <experience></experience>
    <projects></projects>
    <skills></skills>
    <interests></interests>
    <contact></contact>
  </div>
  <site-footer></site-footer>
</div>
</template>

<script>
import About from './components/About'
import Academics from './components/Academics'
import Contact from './components/Contact'
import Experience from './components/Experience'
import Interests from './components/Interests'
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
    Interests,
    NavBar,
    Projects,
    SiteFooter,
    Skills,
    Welcome
  }
}
</script>

<style lang="sass">
@import './styles.scss';

h1 {
  text-align: center;
  font-weight: 600;
  &.hero-heading {
    font-size: 100px;
  }
}

a {
  color: $viridian;
}

body {
  font-family: 'Alegreya Sans', sans-serif;
  position: relative;
  // color: $jelly-bean;
  // background-color: $cabaret;
}

::selection {
  text-shadow: none;
  background: rgba($cabaret, 0.25);
}

.no-margin {
  margin: 0;
}

.align-right {
  text-align: right;
}

.align-left {
  text-align: left;
}

@keyframes fadeIn { from { opacity:0; } to { opacity:1; } }

.in-view {
  opacity:0;
	animation:fadeIn ease-in 1;
	animation-fill-mode:forwards;
	animation-duration:1s;
}

/* Shared
–––––––––––––––––––––––––––––––––––––––––––––––––– */
.button {
  border-radius: 100px;
  margin-bottom: 0;
  &-standalone {
    margin: 0 1rem;
  }
}

/* Sections
–––––––––––––––––––––––––––––––––––––––––––––––––– */
section {
  /*padding: 8rem 0 7rem;*/
  padding: 12rem 0;
  text-align: center;
}
.section {
  &-even {
    /*background-color: #041E42;*/
    background-color: $amber;
    background-position: center;
    background-repeat: no-repeat;
  }
  &-heading,
  &-description {
    margin-bottom: 1.2rem;
  }
}

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
