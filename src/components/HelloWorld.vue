<template>
  <div class="hello">
    <!--<div class="menu">-->
      <!--<ul>-->
        <!--<li> PREDICT</li>-->
        <!--<li> FORMATION</li>-->
      <!--</ul>-->
    <!--</div>-->
    <div id="main">
      <nav :class="active" v-on:click.prevent>
        <a href="#" class="home" v-on:click="makeActive('home')">Home</a>
        <a href="#" class="projects" v-on:click="makeActive('projects')">Projects</a>
        <a href="#" class="services" v-on:click="makeActive('services')">Services</a>
        <a href="#" class="contact" v-on:click="makeActive('contact')">Contact</a>
        <div :class="borderClass"></div>
      </nav>
    </div>

    <!--<div  id="vue-app">-->
      <!--<div id="bag" :class="{burst:ended}">-->

      <!--</div>-->
      <!--<div id="bag-health">-->
          <!--<div :style="{width: health + '%'}">-->
          <!--</div>-->
      <!--</div>-->
      <!--<div id="controls">-->
        <!--<button @click="punch" v-show="!ended"> Punch</button>-->
        <!--<button @click="restart"> Restart </button>-->
      <!--</div>-->
    <!--</div>-->
  </div>
</template>

<script type="text/babel">
export default {
  name: 'HelloWorld',
  data () {
    return {
      active: 'home'
    }
  },
  methods: {
    makeActive (item) {
      this.active = item
    }
  },
  computed: {
    borderClass () {
      if (this.active === 'home') {
        return 'border-bottom'
      } else if (this.active === 'projects') {
        return 'border-bottom projects-tab'
      }
    }
  }
}
</script>
