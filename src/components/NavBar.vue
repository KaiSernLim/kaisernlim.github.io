<template id="navbar">
  <nav id="navbar">
    <ul class="nav">
      <!-- <div class="container"> -->
        <li id="logo"><a href="#about">Kai-Sern Lim</a></li>
        <div id="nav-links">
          <li><a href="#academics" class="button">Academics</a></li>
          <li><a href="#experience" class="button">Experience</a></li>
          <li><a href="#projects" class="button">Projects</a></li>
          <li><a href="#skills" class="button">Skills</a></li>
          <li><a href="#interests" class="button">Interests</a></li>
          <li><a href="#contact" class="button">Contact</a></li>
        </div>
      <!-- </div> -->
    </ul>
  </nav>
</template>

<style lang="sass">
@import '../styles.scss';

#navbar {
  ul {
    position: fixed;
    top: 0;
    width: 100%;
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: transparent;
    z-index: 1101;
    & #nav-links {
      float: right;
      margin: 10px;
    }
  }

  li {
    float: left;
    margin: 2px;
    #logo {
      float: left;
    }
    a {
      display: block;
      color: black;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
      &:hover {
        background-color: $viridian !important;
        color: white;
      }
    }
    &.active {
      > a {
        background-color: $jelly-bean;
        color: white;
      }
    }
  }

  .button {
    padding-top: 2px;
    border: none;
  }
}
</style>
