<template>
    <div class="container"> 
        <nav class="navbar navbar-expand-lg navbar-light bg-light"
            v-if="$route.name !='login' && $route.name !='register' ">
            <div class="collapse navbar-collapse">
                <div class="navbar-nav">
                    <router-link to="/all" class="nav-item nav-link">Order List</router-link>
                    <router-link to="/create" class="nav-item nav-link">Create Order</router-link>
                </div>
            </div>
        </nav>

        <router-view> </router-view>
    </div>
</template>
 
<script>
    export default {
    }
</script>