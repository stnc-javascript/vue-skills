<template>
    <div class="about">
        <p>Hellow {{ name }}</p>
        This is the about page
    </div>
</template>

<script>
    export default {
        data () {
            return {
                name: this.$route.params.name
            }
        }
    }
</script>
