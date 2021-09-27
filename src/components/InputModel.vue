<template>
    <div>
        <input type="text" v-model="itemPlaceholder" @keypress.enter="eventFire"/>
        <button @click="eventFire">Ekle</button>
    </div>
</template>

<script>
export default {
    name:'InputModel',
    data(){
        return{
            itemPlaceholder:''
        }
    },
    methods:{
        eventFire(){            
            this.$emit('catchItem',this.itemPlaceholder);
        }
    }
}
</script>