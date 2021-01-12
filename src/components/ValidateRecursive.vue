<template>
    <div>
        <slot></slot>
    </div>
</template>

<script>
  import Validate from "./Validate";

  export default {
    name: "ValidateRecursive",
    extends: Validate,
    
    mounted () {
      this.getChildren(this, (p, i) => i.validator(p, i));
    },
    
    methods: {
      getChildren (instance, func) {
        for (const childInstance of instance.$children) {
          if (instance.$options.name === childInstance.$options.name) {
            func(instance, childInstance);
          } else {
            this.getChildren(childInstance, func);
          }
        }
      }
    }
  };
</script>

<style scoped>

</style>
