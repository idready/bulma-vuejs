<template>
  <footer class="footer">
    <div class="content has-background-red has-text-centered">
      <p>Philosophers @{{date}}</p>
    </div>
  </footer>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class FooterComponent extends Vue {
  public date: number;

  constructor() {
    super();
    this.date = new Date().getUTCFullYear();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

  @import '../../sass/_custom.scss';

  footer {
    padding: 1rem 1.5rem;
  }

</style>
