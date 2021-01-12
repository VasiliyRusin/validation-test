<template>
    <div>
        <slot></slot>
    </div>
</template>

<script>
  export default {
    name: "Validate",
    
    props: {
      // Just for demonstration purposes
      id: {
        type: String,
        required: true
      }
    },
    
    methods: {
      validator: (p, i) => console.log(p.id, i.id)
    }
  };
</script>

<style scoped>

</style>
