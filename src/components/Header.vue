<template>
        <header>
        <h1>{{ title }}</h1> 
        <Button btnname="Add Task" color="green" />
    </header>
   
</template>
<script>
import Button from './Button.vue';
export default ({
    components: {
       Button,
  },
    props:{
        title:String,
    },
    name: 'Header'
})
</script>
<style scoped>
header{
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
    align-items: center;
}
</style>