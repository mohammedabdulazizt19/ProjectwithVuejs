<script>
import Login from './components/LogIn.vue'
import HelloWorld from './components/HelloWorld.vue'
import NotFound from './components/NotFound.vue'

const routes = {
  '/': Login,
  '/hello-world': HelloWorld
}

export default {
  data() {
    return {
      currentPath: window.location.hash
    }
  },
  computed: {
    currentView() {
      return routes[this.currentPath.slice(1) || '/'] || NotFound
    }
  },
  mounted() {
    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
		})
  }
}
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#/">Login</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#/hello-world">Hello World</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<div class="container mt-3">
  <component :is="currentView" />
</div>
</template>