<template>
<div>
    
    <h3>{{counter}}</h3>
    <h3>{{doubleval}}</h3>
    <button @click="increment">Count is: {{counter}}</button>
     <!-- <h3>{{user.name}}</h3>
    <h3>{{user.age}}</h3> -->
    <h3>{{name}}</h3>
    <h3>{{age}}</h3>
    
</div>
</template>

<script>
import { reactive,toRefs,computed, } from 'vue';

export default {
    setup() {
        // let counter = ref(0);
        // counter.value;
        const user=reactive(
            {
                name:"Ehsan ",
                age:27,
                counter:0
            }
        )
        setTimeout(() => {
            // counter.value++,
            user.name="Ali",
            user.age=28
        
        }, 2000);
        const data=toRefs(user);
        function increment(){
            user.counter++;
            if(user.counter==5){
                user.counter=0;
            }
        }
        const doubleval=computed(()=>{
            return user.counter*2
        })
        
      
        return {
            counter:0,
            // user
            // ...toRefs(user),
            ...data,
            user,
            increment,
            doubleval,
            
            

        }
    

}
}
</script>
