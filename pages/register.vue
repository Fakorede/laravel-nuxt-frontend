<template>
    <div class="container col-md-6 mt-5">
        <h2>Register</h2>
        <br>
        <form>
            <div class="form-group">
                <label>Full Name</label>
                <input type="text" class="form-control" placeholder="Enter your name">
                <small class="form-text text-danger">Show error messages</small>
            </div>
            <div class="form-group">
                <label>Email address</label>
                <input type="email" class="form-control" placeholder="Enter email">
                <small class="form-text text-danger">Show error messages</small>
            </div>
            <div class="form-group">
                <label>Password</label>
                <input type="password" class="form-control" placeholder="Password">
                <small class="form-text text-danger">Show error messages</small>
            </div>
            <button type="submit" class="btn btn-primary">Register</button>
        </form>
        <br>
        <p>Already have an account? <nuxt-link to="/register">Login</nuxt-link></p>
    </div>
</template>

<script>
export default {};
</script>

<style>
</style>
