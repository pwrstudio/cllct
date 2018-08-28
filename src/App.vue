<template>
  <div id="app">

    <div id='main'
         class='navigation'
         :class='{"about": about, "menu": menu, "text": text }'>
      <div id='logo'
           class='navigation'
           @click='about = !about'>CLLCT</div>
      <div id='menu'
           class='navigation'
           @click='menu = !menu'>
        <div></div>
        <div></div>
        <div></div>
      </div>

      <div id='left'
           class='navigation'
           @click='prevSlide'></div>
      <div id='right'
           class='navigation'
           @click='nextSlide'></div>
      <div id='down'
           class='navigation'
           @click='text = true'></div>
      <div id='up'
           class='navigation'
           v-if='text'
           @click='text = false'></div>

      <span id='close-menu'
            v-if='about'></span>
      <span id='close-about'
            v-if='menu'></span>

      <div class='carousel-container'>
        <carousel :per-page="1"
                  ref='covercar'
                  :loop='true'
                  :paginationEnabled='false'>
          <slide>
            <img src='./assets/test.jpg' />
          </slide>
          <slide>
            <img src='./assets/test3.jpg' />
          </slide>
          <slide>
            <img src='./assets/test4.png' />
          </slide>
          <slide>
            <img src='./assets/test5.jpg' />
          </slide>
          <slide>
            <img src='./assets/test6.jpg' />
          </slide>
          <slide>
            <img src='./assets/test7.jpg' />
          </slide>
        </carousel>
      </div>

      <div class='text-container'>
        <p>
          <strong>cllct.codes</strong> is a residency dedicated to art collectors.</p>
        <p>Reintroducing the work of art directly into the domestic context, cllct.codes creates intimate and powerful encounters through short residential stay.</p>
        <p>Further events are thought within the residency aiming to contribute to the discovery of local artistic and artisanal production through the historical and cultural heritage of the Monegasque territory and its surroundings, questioning and revealing its patrimony to the public through contemporary reflexions and interventions. </p>
      </div>

    </div>

    <div id='menu-container'>
      <section class='year-2018'>
        <div class='year'>2018</div>
        <!-- <div class='divider' /> -->
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
      </section>
      <section class='year-2017'>
        <div class='year'>2017</div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
      </section>

      <section class='year-2016'>

        <div class='year'>2016</div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
      </section>

      <section class='year-2015'>

        <div class='year'>2015</div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
        <div class='event'
             @click='menu = false'>
          <div>10/10 – 11/11</div>
          <div>Name Surname</div>
          <div>Title</div>
        </div>
      </section>
    </div>

    <div id='about-container'>
      <article>
        <p>
          <strong>cllct.codes</strong> is a residency dedicated to art collectors.</p>
        <p>Reintroducing the work of art directly into the domestic context, cllct.codes creates intimate and powerful encounters through short residential stay.</p>
        <p>Further events are thought within the residency aiming to contribute to the discovery of local artistic and artisanal production through the historical and cultural heritage of the Monegasque territory and its surroundings, questioning and revealing its patrimony to the public through contemporary reflexions and interventions. </p>
      </article>

      <article>
        <div class='divider' />
        <p>Mail<br/> Twitter
          <br/> Instagram
          <br/> Facebook
        </p>
      </article>

      <article>
        <div class='divider' />
        <p>
          <strong>Supported by</strong>
        </p>
      </article>

    </div>

  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      menu: false,
      about: false,
      text: false
    }
  },
  methods: {
    nextSlide() {
      this.$refs.covercar.goToPage(this.$refs.covercar.currentPage + 1)
      if (this.$refs.covercar.canAdvanceForward) {
        this.canGoForward = true
      } else {
        this.canGoForward = false
      }
      if (this.$refs.covercar.currentPage === 0) {
        this.canGoBack = false
      } else {
        this.canGoBack = true
      }
    },
    prevSlide() {
      this.$refs.covercar.goToPage(this.$refs.covercar.currentPage - 1)
      if (this.$refs.covercar.canAdvanceForward) {
        this.canGoForward = true
      } else {
        this.canGoForward = false
      }
      if (this.$refs.covercar.currentPage === 0) {
        this.canGoBack = false
      } else {
        this.canGoBack = true
      }
    }
  }
}
</script>

<style lang="scss">
html,
body {
  margin: 0;
  padding: 0;
}

#app {
  font-family: 'Wremena', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: black;
  font-weight: 300;
  margin: 0;
  padding: 0;
}

#main {
  position: fixed;
  top: 0;
  left: 0;
  height: 200vh;
  width: 100vw;
  background: white;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  padding: 0;
  box-shadow: 0px 0px 20px black;
  // transition: transform 0.2s ease-out;
  transition: all 400ms cubic-bezier(0.23, 1, 0.32, 1);
  z-index: 100;
  &.menu {
    transform: translateX(-50vw);
    // transition: transform 0.2s ease-out;
    transition: all 400ms cubic-bezier(0.23, 1, 0.32, 1);
    .navigation {
      opacity: 0;
    }
    .VueCarousel {
      pointer-events: none;
    }
  }
  &.about {
    transform: translateX(50vw);
    // transition: transform 0.2s ease-out;
    transition: all 400ms cubic-bezier(0.23, 1, 0.32, 1);
    .navigation {
      opacity: 0;
    }

    .VueCarousel {
      pointer-events: none;
    }
  }

  &.text {
    transform: translateY(-100vh);
    // transition: transform 0.2s ease-out;
    transition: all 400ms cubic-bezier(0.23, 1, 0.32, 1);
    // .navigation {
    //   opacity: 0;
    // }

    .VueCarousel {
      pointer-events: none;
    }
  }
}

#logo {
  position: fixed;
  top: 20px;
  left: 20px;
  font-size: 72px;
  z-index: 1000;
  cursor: pointer;
  &:hover {
    font-weight: normal;
  }
}

.navigation {
  cursor: pointer;
}

#left {
  width: 40px;
  height: 40px;
  border-bottom: 2px solid black;
  border-left: 2px solid black;
  position: fixed;
  margin-top: -30px;
  top: 50vh;
  left: 40px;
  transform: rotateZ(45deg);
  z-index: 1000;

  cursor: pointer;
  &:hover {
    border-bottom: 4px solid black;
    border-left: 4px solid black;
  }
}

#close-menu {
  width: 60px;
  height: 60px;
  position: fixed;
  top: 20px;
  left: 20px;
  pointer-events: none;
  z-index: 1000;
}

#close-menu:after {
  content: '';
  height: 60px;
  border-left: 2px solid #000;
  position: absolute;
  transform: rotate(45deg);
  left: 28px;
  z-index: 1000;
}

#close-menu:before {
  content: '';
  height: 60px;
  border-left: 2px solid #000;
  position: absolute;
  transform: rotate(-45deg);
  left: 28px;
}

#close-about {
  width: 60px;
  height: 60px;
  position: fixed;
  top: 20px;
  right: 30px;
  pointer-events: none;
}

#close-about:after {
  content: '';
  height: 60px;
  border-left: 2px solid #000;
  position: absolute;
  transform: rotate(45deg);
  left: 28px;
}

#close-about:before {
  content: '';
  height: 60px;
  border-left: 2px solid #000;
  position: absolute;
  transform: rotate(-45deg);
  left: 28px;
}

#right {
  width: 40px;
  height: 40px;
  border-bottom: 2px solid black;
  border-left: 2px solid black;
  position: fixed;
  top: 50vh;
  margin-top: -30px;
  right: 40px;
  transform: rotateZ(225deg);
  z-index: 1000;

  &:hover {
    border-bottom: 4px solid black;
    border-left: 4px solid black;
  }
}

#down {
  width: 40px;
  margin-left: -30px;
  height: 40px;
  border-bottom: 2px solid black;
  border-left: 2px solid black;
  position: fixed;
  top: 90vh;
  left: 50%;
  transform: rotateZ(-45deg);
  z-index: 1000;

  &:hover {
    border-bottom: 4px solid black;
    border-left: 4px solid black;
  }
}

#up {
  width: 40px;
  margin-left: -30px;
  height: 40px;
  border-bottom: 2px solid black;
  border-left: 2px solid black;
  position: fixed;
  top: calc(100vh);
  left: 50%;
  transform: rotateZ(135deg);
  z-index: 1000;

  &:hover {
    border-bottom: 4px solid black;
    border-left: 4px solid black;
  }
}

#menu {
  width: 60px;
  height: 60px;
  position: fixed;
  top: 25px;
  right: 30px;
  z-index: 1000;

  div {
    border-bottom: 2px solid black;
    margin-top: 12px;
  }

  &:hover {
    div {
      border-bottom: 4px solid black;
      margin-top: 10px;
    }
  }
}

img {
  // max-width: 80vw;
  // min-width: 80vh;
  // display: block;
}

#menu-container {
  position: fixed;
  top: 0;
  right: 0;
  height: 100vh;
  width: 50vw;
  background: rgba(0, 0, 0, 0.1);
  font-size: 72px;
  text-transform: uppercase;
  text-align: center;
  overflow: auto;
}

#about-container {
  position: fixed;
  top: 0;
  left: 0;
  height: 100vh;
  width: 50vw;
  overflow: auto;
  background: rgba(0, 0, 0, 0.1);
  font-size: 22px;
  overflow: auto;
  font-weight: normal;
  article {
    padding: 20px;
  }
}

.divider {
  width: 100%;
  border-bottom: 2px solid black;
}

.carousel-container {
  height: 100vh;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
}

.text-container {
  height: 100vh;
  width: 100vw;
  position: absolute;
  top: 100vh;
  left: 0;
  overflow: auto;
  p {
    font-size: 32px;
    width: 70vw;
    margin-right: auto;
    margin-left: auto;
  }
}

.VueCarousel {
  height: 100vh;
}

.VueCarousel-slide {
  display: flex;
  justify-content: center;
  align-items: center;
  img {
    max-height: 80vh;
    max-width: 80vw;
  }
}

.VueCarousel-pagination {
  display: none;
}

.year {
  font-weight: normal;
}

.event {
  margin-bottom: 20px;
  cursor: pointer;
  &:hover {
    color: white;
  }
}

.year-2018 {
  background: #5f4a8b;
  display: inline-block;
  width: 100%;
}
.year-2017 {
  background: #93b757;
  display: inline-block;
  width: 100%;
}
.year-2016 {
  background: #f6cac9;
  display: inline-block;
  width: 100%;
}
.year-2015 {
  background: #985051;
  display: inline-block;
  width: 100%;
}

.VueCarousel-wrapper,
.VueCarousel-inner {
  height: 100vh;
}
</style>
