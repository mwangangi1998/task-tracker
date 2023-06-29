<template>
<div>
   <div :class="[task.reminder ? 'reminder' :'','task']">
    <h3>{{ task.text }} <i class="fas fa-times"></i></h3>
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
.task reminder{
    border-left: 5px solid green;
}
.task h3 {

    display: flex;
    padding: 12px;
    align-items: center;
    justify-content: space-between;
}
</style>