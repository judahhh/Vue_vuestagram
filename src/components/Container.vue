<template>

<div>
    <Post :인스타데이터="인스타데이터[i]" v-for="(a,i) in 인스타데이터" :key="i"/>
    
</div>

</template>

<script>
import Post from './Post.vue';


export default{ 
name:'Container',
components:{
    Post,
},
props:{
인스타데이터:Array,
},
data(){
    return{
};
    },
    setup(){},
    created(){},
    mounted(){},
    unmounted(){},
    methods:{}
}
</script>

<style>
</style>