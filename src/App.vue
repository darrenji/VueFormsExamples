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
                    
                    <div class="row">
<!--                        <textarea>{{message}}</textarea> 这样的写法是不行的-->
                        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                            <label for="message">Message</label>
                            <textarea 
                                id="message" 
                                rows="5" 
                                class="form-control"
                                v-model="message"></textarea>
                        </div>
                    </div>
                    
                    <div class="row">
                        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                            <div class="form-group">
                                <label for="sendmail">
                                    <input type="checkbox" id="sendmail" value="SendMail" v-model="sendMail"> Send Mail
                                </label>
                                <label for="sendInfomail">
                                    <input type="checkbox" id="sendInfomail" value="SendInfoMail" v-model="sendMail"> Send Infomail
                                </label>
                            </div>
                        </div>
                    </div>
                    
                    <div class="row">
                        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                            <label for="male">
                                <input type="radio" id="male" value="Male" v-model="gender"> Male
                            </label>
                            <label for="female">
                                <input type="radio" id="female" value="Female" v-model="gender"> Female
                            </label>
                        </div>
                    </div>
                    
                    
                    <div class="row">
                        <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                            <label for="priority">Priority</label>
<!--                            select中v-model的优先级要高于option中:selected的优先级-->
                            <select id="priority"
                                   class="form-control"
                                   v-model="selectedPriority">
                                 <option 
                                     v-for="item in  priorities" 
                                     :selected="item=='Medium'">{{item}}</option>   
                            </select>
                        </div>
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
                        <p style="white-space:pre">Message:{{message}}</p>
                        <p><strong>Send Email?</strong></p>
                        <ul>
                            <li v-for="item in sendMail">{{ item }}</li>
                        </ul>
                        <p>Gender:{{gender}}</p>
                        <p>Priority:{{selectedPriority}}</p>
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
                },
                message: 'A new Text',
                sendMail: [],
                gender: 'Male',
                selectedPriority: 'High',
                priorities: ['High', 'Medium', 'Low']
            }
        }
    }
</script>

<style>

</style>
