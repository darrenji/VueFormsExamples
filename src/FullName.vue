<template>
    <div>
        <div class="form-group">
            <label for="firstName">First Name</label>
            <input type="text" v-model="value.firstName" class="form-control" id="firstName" placeholder="First Name">
        </div>
        <div class="form-group">
            <label for="lastName">Last Name</label>
            <input type="text" v-model="value.lastName" class="form-control" id="lastName" placeholder="Last Name">
        </div>
    </div>
</template>


<script>
    export default {
        props: ['value'],
        watch: {
            'value.firstName': function(){
                this.$emit('input', this.value);
            },
            'value.lastName': function(){
                this.$emit('input', this.value);
            }
        }
    }
</script>