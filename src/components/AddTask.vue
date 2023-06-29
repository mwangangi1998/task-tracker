<template>
    <form class="add-form">
        <div class="form-group">
            <input type="text" id="text" v-model="text"  placeholder="Add Task" >
        </div>
        <div class="form-group">
            <input type="text" id="day"  v-model="day" placeholder="Add Day and time" >
        </div>
        <div class="form-group ">
           <Label> set reminder<input type="checkbox"  id="reminder" v-model="reminder"  placeholder="Add Day and time" ></Label>
        </div>
        <div class="form-group">
            <input type="submit" class="btn" >
        </div>
    </form>
</template>

<script>
export default{
    name: 'AddTask',
    props:{
        AddTask:String,
    },
    data() {
        return {
            text:'',
            day:'',
            reminder:false,
        }
    },
}

</script>
<style scoped>
input{
    width: 100%;
    height: 30px;
   color: rgb(4, 1, 1);
    
}
.btn{
    background: #2040cf;
    color:white;
}
.form-group{
    padding-top: 20px;
}
</style>