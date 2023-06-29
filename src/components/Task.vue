<template>
<div>
   <div 
   :class="[task.reminder ? 'reminder' : '','task']" @dblclick="$emit('toggle-reminder',task.id)"
   >
    <h3>{{ task.text }} <i @click="($emit('delete-task',task.id))" class="fas fa-times"></i></h3>
    <p>{{ task.day }}</p>
   </div>
</div>
</template>
<script>
export default{
    props:{
        task: Object,
    },
    name: 'Task',
    
}


</script>
<style>
.fas{
    color: crimson;
}
.task{
    background: #f4f4f4;
    margin: 5px;
    pad: 10px 20px;
    cursor: pointer;
}
.task.reminder{
    border-left: 5px solid green;
}
.task h3 {

    display: flex;
    padding: 12px;
    align-items: center;
    justify-content: space-between;
}
</style>