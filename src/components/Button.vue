<template>
    <button @click="onClick()"
    :style="{ background: color }" 
    class="btn">{{ btnname }}</button>
</template>
<script>
export default {
    props: {
        btnname: String,
        color: String
    },
    data() {
        return {
            name: 'Button'
        }
    },
    methods: {
        onClick(){
            console.log('button clicked')
        }
    },
}
</script>
<style></style>