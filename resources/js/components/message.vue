<template>
<div>
        <li class="list-group-item" :class="messageColor"><slot></slot></li>
        <small class="bagde float-right badge-primary">You </small>

</div>
</template>

<script>
    export default {
        props:[
            'color'
        ],
        computed:{
            messageColor(){
                return 'list-group-item-'+this.color;
            },
            badgeClass(){
                return 'badge-'+this.color;
            }
        },

        mounted() {
            console.log('Component mounted.')
        }
    }
</script>
