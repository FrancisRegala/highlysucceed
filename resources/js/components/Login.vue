<template>
    <div class="hold-transition login-page">
        <div class="login-box">
            <!-- /.login-logo -->
            <div class="card card-outline card-primary">
                <div class="card-header text-center">
                <a href="#" class="h1"><b>BE Practical</b> Exam</a>
                </div>
                <div class="card-body">
                <p class="login-box-msg">Sign in to start your session</p>

                <form action="../../index3.html" method="post">
                    <div class="input-group mb-3">
                    <input type="email" v-model="email" class="form-control" placeholder="Email">
                    <div class="input-group-append">
                        <div class="input-group-text">
                        <span class="fas fa-envelope"></span>
                        </div>
                    </div>
                    </div>
                    <div class="input-group mb-3">
                    <input type="password" v-model="password" class="form-control" placeholder="Password">
                    <div class="input-group-append">
                        <div class="input-group-text">
                        <span class="fas fa-lock"></span>
                        </div>
                    </div>
                    </div>
                    <div class="row">
                        <div class="col-6">
                            <div class="icheck-primary">
                            <input type="checkbox" id="remember">
                                <label for="remember">
                                    Remember Me
                                </label>
                            </div>
                        </div>
                        <div class="col-6">
                            <div class="icheck-primary float-right">
                                <router-link to="/register" >Registration</router-link>
                            </div>
                        </div>
                    </div>
                </form>

                <div class="social-auth-links text-center mt-2 mb-3">
                    <a href="#" class="btn btn-block btn-primary"
                        @click="signIn()">
                    <i class="fab fa-sign mr-2"></i> Sign in 
                    </a>
                </div>
                </div>
                <!-- /.card-body -->
            </div>
            <!-- /.card -->
        </div>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                email: '',
                password: ''
            }
        },
        created() {
        },
        methods: {
            signIn() { 
                
                if(this.email == 'pantet008@gmail.com' && this.password == 'pass123'){
                    //alert('success');
                    this.$router.push({ name: 'all' });
                } else {
                    alert('Access Denied! Please enter valid email and password.');
                }
            }
        }
    }
</script>