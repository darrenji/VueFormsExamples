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
                            v-model="email">
                    </div>
                    
                    <div class="form-group">
                        <label for="password">Password</label>
                        <input 
                             type="text"
                             class="form-control"
                             id="password">
                    </div>
                    
                    <div class="form-group">
                        <label for="">Age</label>
                        <input 
                              type="text" 
                              id="age"
                              class="form-control">
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
                        <p>Email:{{email}}</p>
                        <p>Password:</p>
                        <p>Age:</p>
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
                email: ''
            }
        }
    }
</script>

<style>

</style>
