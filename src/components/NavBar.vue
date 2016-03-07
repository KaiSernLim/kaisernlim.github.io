<template>
<nav id="navbar">
  <ul class="nav">
    <div class="container">
      <logo></logo>
      <div id="nav-links">
        <li><a href="#academics" class="button">Academics</a></li>
        <li><a href="#experience" class="button">Experience</a></li>
        <li><a href="#projects" class="button">Projects</a></li>
        <li><a href="#skills" class="button">Skills</a></li>
        <li><a href="#interests" class="button">Interests</a></li>
        <li><a href="#contact" class="button">Contact</a></li>
      </div>
    </div>
  </ul>
</nav>
</template>

<script>
import Logo from './Logo'

export default {
  components: {
    Logo
  }
}
</script>

<style lang="sass">
@import '../assets/css/styles.scss';

/* Styling
–––––––––––––––––––––––––––––––––––––––––––––––––– */
#navbar {
  ul {
    position: fixed;
    top: 0;
    width: 100%;
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: rgba(white, 0.9);
    z-index: 1101;
  }
}

#nav-links {
  float: right;
  margin: 1.4rem;

  li {
    float: left;
    margin: 2px;

    a {
      display: block;
      color: $nile-blue;
      text-align: center;
      padding: 2px 16px 16px 16px;
      text-decoration: none;
      border: none;

      &:hover {
        background-color: $bittersweet !important;
        color: $sugar-cane;
        transition: 0.2s ease-in;
      }
    }

    &.active {
      > a {
        background-color: $nile-blue;
        color: $sugar-cane;
      }
    }
  }
}
</style>
