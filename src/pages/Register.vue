<template>
    <div class="register-container">
        <div class="register-form-container">
            <form id="registerForm" novalidate autocomplete="off">
                <h3>Create your account</h3>
                <div class="form-group">
                    <label for="uName">Enter your name:
                    </label>
                    <input type="text" name="uName" placeholder="your full name" id="uName" class="form-control"
                         />
                </div>

                <div class="form-group">
                    <label for="uEmail">Enter your email:
                    </label>
                    <input type="email" name="uEmail" placeholder="example@gmail.com" id="uEmail" class="form-control"
                     />
                </div>

                <div class="form-group">
                    <label for="uPass">Enter your password:
                    </label>
                    <input type="password" name="uPass" placeholder="enter your password" id="uPass"
                        class="form-control" />
                </div>

                <div class="form-group">
                    <label for="uPassConfirm">Check your password again:
                    </label>
                    <input type="password" name="uPassConfirm" placeholder="enter your password again" id="uPassConfirm"
                        class="form-control"  />
                </div>

                <div class="form-group">
                    <label for="uPhone">Enter your phone number:
                    </label>
                    <input type="tel" name="uPhone" placeholder="enter your phone number" id="uPhone"
                        class="form-control" />
                </div>

                <div class="form-group">
                    <label for="uBirth">Enter your birthday:
                    </label>
                    <input type="date" name="uBirth" id="uBirth" class="form-control" @click="availableTime()"
                       />
        
                </div>

                <div class="form-group">
                    <label for="">Select your gender:
                    </label>
                    <div class="form-group">
                        <input type="radio" name="gender" value="male" id="genderMale"
                           /><span>Male</span>
                        <input type="radio" name="gender" value="female" id="genderFemale"
                           /><span>Female</span>
                    </div>
    
                </div>

                <div class="form-group">
                    <input type="submit" value="join us" class="btn" />
                    <p>have an account? <router-link @click="scrollToTop()" to="/login">login</router-link>
                    </p>
                </div>
            </form>
        </div>
    </div>
</template>


<script>
export default {
    name: "Home",

    methods: {
        scrollToTop() {
            window.scrollTo(0, 0);
        }
    }
};
</script>

<style scoped>
.register-container {
    padding: 2rem 9%;
}

.register-container .register-form-container {
    background: #fff;

}

.register-container .register-form-container form {
    position: relative;
    left: 50%;
    transform: translate(-50%, 0%);
    max-width: 70rem;
    width: 100%;
    box-shadow: 0 1rem 1rem rgba(0, 0, 0, 0.05);
    border: 0.1rem solid rgba(0, 0, 0, 0.2);
    padding: 2rem;
    border-radius: 0.5rem;
    animation: fadeUp 0.4s linear;
}

.register-container .register-form-container form h3 {
    padding-bottom: 1rem;
    font-size: 2rem;
    text-transform: uppercase;
    color: #130f40;
    margin: 0;
}

.register-container .register-form-container form .form-control {
    margin: 0.7rem 0;
    border-radius: 0.5rem;
    background: #f7f7f7;
    padding: 2rem 1.2rem;
    font-size: 1.6rem;
    color: #130f40;
    text-transform: none;
    width: 100%;
    border: none;
}

.register-container .register-form-container form label {
    font-size: 2rem;
    margin: 0;
    padding: 0;
}

.register-container .register-form-container form span {
    font-size: 18px;
    padding-left: 5px;
    padding-right: 40px;
}

.register-container .register-form-container form .btn {
    margin: 1rem 0;
    width: 100%;
    text-align: center;
}

.register-container .register-form-container form p {
    padding-top: 1rem;
    font-size: 1.5rem;
    color: #666;
    margin: 0;
}

.register-container .register-form-container form p a {
    color: #27ae60;
}

.register-container .register-form-container form p a:hover {
    color: #130f40;
    text-decoration: underline;
}

.register-container .register-form-container form .form-group {
    margin: 0;
}

.register-container .register-form-container form .form-group .error-mess {
    font-size: 1.5rem;
    position: relative;
    color: rgb(243, 47, 47);
    margin: 0;
    padding: 0;
}
</style>
