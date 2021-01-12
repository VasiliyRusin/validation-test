<template>
    <div>
        <slot></slot>
    </div>
</template>

<script>
  import Validate from "./Validate";

  export default {
    name: "ValidateProvideInject",
    extends: Validate,
  
    provide () {
      return {
        parent: this
      };
    },

    inject: {
      parent: { default: undefined }
    },
    
    mounted () {
      if (this.parent?.$options.name === this.$options.name) {
        this.validator(this.parent, this);
      }
    }
  };
</script>

<style scoped>

</style>
