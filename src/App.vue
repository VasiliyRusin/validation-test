<template>
    <main>
        <Validate id="1">
            <Validate id="2">
                <Validate id="4"></Validate>
                <Validate id="5"></Validate>
            </Validate>
            <Validate id="3"></Validate>
        </Validate>
    </main>
</template>

<script>
  // import ValidateRecursive from "@/components/ValidateRecursive";
  import ValidateProvideInject from "@/components/ValidateProvideInject";
  
  export default {
    name: 'App',
    components: { Validate: ValidateProvideInject }
  }
</script>

<style></style>
