<template>
    <form class="add-form" @submit="onSub">
        <div class="form-group">
            <input type="text" id="text" v-model="text"  placeholder="Add Task" >
        </div>
        <div class="form-group">
            <input type="text" id="day"  v-model="day" placeholder="Add Day and time" >
        </div>
        <div class="form-group ">
           <Label > set reminder</Label><input type="checkbox"  id="reminder" v-model="reminder"  placeholder="Add Day and time" >
        </div>
        <div class="form-group">
            <input type="submit" value="Add Task" class="btn" >
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
    methods: {
        onSub(e){
            e.preventDefault()
            if (!this.text ) {
                alert('Add Task')
                return;
            }
            const newTask={
                // id: Math.floor(Math.random()*100000),
                text: this.text,
                day: this.day,
               reminder: this.reminder,
            }
            this.$emit('add-task',newTask);
            this.text='',
            this.day='',
            this.reminder=false
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
Label{
    
    font-weight: bolder; 
   text-transform: capitalize;
}
.btn{
    background: #2040cf;
    color:white;
}
#reminder{
    height: 23px;
}
.form-group{
    padding-top: 20px;
}
</style>