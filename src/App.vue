<template>
    <div class="container">
        <form>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <full-name v-model="userData.fullname"></full-name>
                </div>
            </div>
        </form>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>Full Name: {{userData.fullname.firstName + " " + userData.fullname.lastName}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>


<script>
    import fullName from './FullName.vue';
    export default {
        data(){
            return {
                userData: {
                    fullname: {
                        firstName: '',
                        lastName: '',
                    },
                    email: "",
                    password: "",
                    storeData: true
                },
                submitted: false
            }
        },
        components: {
            fullName: fullName
        },
        methods: {
            submit(){
                this.submitted = true;
            }
        }
    }
</script>


<style>

</style>