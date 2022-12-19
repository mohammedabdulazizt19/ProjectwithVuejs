<template>
    <div class="col-md-10 card flex-row mx-auto px-0">
        <div class="card-body p-5">
            <h4 class="mb-5 text-center mt-4">      
                Yaramay
            </h4>
            <hr class="my-4" />
            <form class="form-box px-3">
                <div class="form-input">
                    <span><i class="fa fa-envelope-o"></i></span>
                    <input type="email" placeholder="Username" tabindex="10" required>
                </div>
                <div class="form-input mb-4">
                    <span><i class="fa fa-key"></i></span>
                    <input type="password" placeholder="password" required>
                </div>
                <div class="d-grid gap-2 col-6 mx-auto mb-3">
                    <button type="submit" class="btn btn-success btn-lg text-uppercase">Login</button>
                </div>
                <div class="mt-5 text-start">
                    <label class="form-label"><a href="#">forget password</a></label>
                </div>
                <div class="mb-3 text-start">
                    <label class="form-label">no account? <a href="#">Sign up</a></label>
                </div>
            </form>
        </div>
    </div>

</template>
<script>
export default {
    name: 'LogIn'
}
</script>

<style>
body{
    background: #3fb37f;
}

.login-form{
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.card{
    overflow: hidden;
    border: 0 !important;
    border-radius: 20px !important;
    box-shadow: 0 0.5rem 1rem 0 rgba(0, 0, 0, 0.1);
}

.form-input{
    position: relative;
}

.form-input input{
    width: 100%;
    height: 45px;
    padding-left: 40px;
    margin-bottom: 20px;
    box-sizing: border-box;
    box-shadow: none;
    border: 1px solid #00000020;
    border-radius: 10px;
    outline: none;
    background: transparent;
}

.form-input span{
    position: absolute;
    top: 10px;
    padding-left: 15px;
    color: #3fb37f;
}

.form-input input::placeholder{
    color: black;
    padding-left: 0px;
}

.form-input input:focus, .form-input input:valid{
    border: 2px solid #3fb37f;
}

.form-input input:focus::placeholder{
    color: #454b69;
}

.custom-checkbox .custom-control-input:checked ~ 
.custom-control-label::before{
    background-color: #007bff !important;
    border: 0px;
}

.form-box button[type="submit"]{
    margin-top: 10px;
    border: none;
    cursor: pointer;
    border-radius: 10px;
    color: #fff;
    font-size: 90%;
    font-weight: bold;
    letter-spacing: .1rem;
    transition: 0.5s;
    padding: 12px;
}
</style>