<template>
  <div class="todo-item">
    <p class="text">{{ todo.text }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
// import Component from 'vue-class-component'; // alternatively

interface Todo {
  [key:string] : any
}

@Component
export default class HelloCode extends Vue {
  // Decorator as @Input() in Angular2+
  @Prop({
    required: true,
    type: Object, // To enforce input type, we have to repeat type here
    // default: 0 // This is used to enforce type checking too
  })
  public todo!: Todo;

  public isLock: boolean = false;

  public keys: {[key: string]: string};

  constructor() {
    super();
    this.keys = {};
  }

  // Can be declare as a simple property
  // data () {
  //   return { lol: false };
  // }
}
</script>

<style scoped lang="scss">
  .text {
    color: darken(#42b983, 10%);
    font-weight: bold;
    font-size: 2rem;
  }
</style>
