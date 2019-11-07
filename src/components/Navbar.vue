
      <template>
  <div>
    <nav class="navbar is-fixed-top" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item">
          <strong>{{itemOne}}</strong>
        </a>
        <a
          role="button"
          class="navbar-burger burger"
          aria-label="menu"
          aria-expanded="false"
          data-target="navbarBasicExample"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div id="navbarBasicExample" class="navbar-menu">
        <div class="navbar-start">
          <a
            class="navbar-item"
            v-for="(item, index) in items"
            :key="index"
            :href="item.url"
          >{{item.title}}</a>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data () {
    return {
      itemOne: 'Jérémie CHABERT',
      items: [
        {
          title: 'A propos',
          url: '#about'
        },
        {
          title: 'Nos biens',
          url: '#properties'
        },
        {
          title: 'Contactez-nous',
          url: '#contact'
        }
      ]
    }
  }
}
</script>

<style scoped>
.navbar {
  background-color: white;
  opacity: 0.7;
}
.navbar-item {
  color: #ff8c3b;
  transition: 0.2s;
}
.navbar-item:hover {
  color: #ff8c3b;
}
</style>
