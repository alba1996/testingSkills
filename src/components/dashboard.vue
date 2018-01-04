<template>
  <div class="dashboard">
    <div class="linear-line"></div>
    <div class="sidebar">
      <div class="search-container">
        <i class="fa fa-search" aria-hidden="true"></i>
        <input type="search" placeholder="Search Here...">
        <h3> Dashboard</h3>
      </div>
      <ul class="main-menu">
        <li>
            <div class="list-item" @click="open">
              <i class="fa fa-user-circle-o" aria-hidden="true"></i>
              <h3>Dashboard</h3>
          <div class="arrow-item">
            <i class="fa fa-angle-up" aria-hidden="true" v-if="!iconActive"></i>
            <i class="fa fa-angle-down" aria-hidden="true" v-if="iconActive"></i>
          </div>
        </div>
          <ul class="submenu">
            <li>
              <router-link to="home" >
                <h3>Project one</h3>
              </router-link>
            </li>
            <li>
              <router-link to="home" >
                <h3>Project two</h3>
              </router-link>
            </li>
          </ul>
        </li>
        <li>
          <router-link to="home">
            <div class="list-item">
              <i class="fa fa-user-circle-o" aria-hidden="true"></i>
              <h3>Project Details</h3>
            </div>
          </router-link>
        </li>
        <li>
          <router-link to="home">
            <div class="list-item">
              <i class="fa fa-user-circle-o" aria-hidden="true"></i>
              <h3>Reviewer Details</h3>
            </div>
          </router-link>
        </li>
        <li>
          <router-link to="home">
            <div class="list-item">
              <i class="fa fa-user-circle-o" aria-hidden="true"></i>
              <h3>Projects</h3>
            </div>
          </router-link>
        </li>
        <li>
          <router-link to="home">
            <div class="list-item">
              <i class="fa fa-user-circle-o" aria-hidden="true"></i>
              <h3>Contact us</h3>
            </div>
          </router-link>
        </li>
      </ul>
    </div>
    <div class="firstBox">
      <h1>PROJECT ONE </h1>


    </div>
  </div>
</template>

<script type="text/babel">
  export default {
    data () {
      return {
        iconActive: false
      }
    },
    methods: {
      open () {
        this.iconActive = !this.iconActive
        console.log(this.iconActive)
      }
    }
  }
</script>
