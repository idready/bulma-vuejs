<template>
  <div>
    <section>
      <p class="notification is-dark has-text-centered is-radiusless">
        <strong>Cookie: </strong> Lorem ipsum dolor sit amet <a class="delete"></a>
      </p>
    </section>
    <section class="container">
      <nav class="navbar" role="navigation" aria-label="main navigation">
        <div class="navbar-brand">
          <a class="navbar-item" href="/">
            <img src="/img/vue.js_logoo.svg" alt="Logo image" width="50" height="50">
          </a>
          <a role="button" class="navbar-burger burger"
          aria-label="menu" aria-expanded="false" data-target="navbarBasicExample">
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
            <span aria-hidden="true"></span>
          </a>
        </div>
        <div id="navbarBasicExample" class="navbar-menu">
          <div class="navbar-start">
            <a class="navbar-item" href="/users">
              Users
            </a>
            <a class="navbar-item" href="/contact">
              Contact
            </a>
          </div>
          <div class="navbar-end">
            <div class="navbar-item">
              <div class="buttons">
                <a class="button is-warning" href="/login">
                  <span class="icon">
                    <i class="fas fa-user"></i>
                  </span>
                  <span>Log in</span>
                </a>
              </div>
            </div>
          </div>
        </div>
      </nav>
    </section>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class HeaderComponent extends Vue {
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  .navbar-item {

    padding: 0.5rem;

    img {
      max-height: none;
    }
  }
</style>
