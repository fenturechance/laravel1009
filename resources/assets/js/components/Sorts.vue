<template>
  <h2>{{sortItems}}</h2>
</template>

<script>
    export default {
        data() {
            return{
                items: [20,23,18,65,32,19,54,56,41]
            }            
        },
        computed: {
            sortItems () {
                return this.items.sort()
            }
        }
    }
</script>