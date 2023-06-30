<template>
        <header>
        <h1>{{ title }}</h1> 
        <Button @toggle-add-task="$emit('toggle-add-task')" 
        :btnname="AddTasks ? 'Close' : 'Add Task'" :color="AddTasks ? 'Red' :'green'" 
        
        />
    </header>
   
</template>
<script>
import Button from './Button.vue';
export default ({
    components: {
       Button,
  },
    props:{
        AddTasks:Boolean,
        title:String,
    },
    name: 'Header',
    // emit:['toggle-add-task'],
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