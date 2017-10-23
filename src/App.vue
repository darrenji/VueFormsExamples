<template>
    <div class="container">
        <form>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <h1>File a Complaint</h1>
                    <hr>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input 
                            type="text"
                            id="email"
                            class="form-control"
                            v-model="userData.email">
                    </div>
                    
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input 
                             type="text"
                             class="form-control"
                             id="password"
                             v-model.lazy="userData.password">
                    </div>
                    
                    <div class="form-group">
                        <label for="">Age</label>
                        <input 
                              type="text" 
                              id="age"
                              class="form-control"
                              v-model="userData.age">
                    </div>
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
                        <p>Email:{{userData.email}}</p>
                        <p>Password:{{userData.password}}</p>
                        <p>Age:{{userData.age}}</p>
                        <p>Message:</p>
                        <p><strong>Send Email?</strong></p>
                        <ul>
                            <li></li>
                        </ul>
                        <p>Gender:</p>
                        <p>Priority:</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                userData:{
                    email: '',
                    password:'',
                    age:27
                }
            }
        }
    }
</script>

<style>

</style>
