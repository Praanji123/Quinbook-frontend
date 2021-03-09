<template>
  <div>
    <center>
      <div class="signup_body">
        <p class="acc_crt">Sign up with QuinBook</p>
        <p class="free_hint">It's free and always will be.</p>
        <form class="signup_form">
          <div>
            <input
              class="firstname"
              v-model="firstName"
              type="text"
              name=""
              placeholder="First name"
            />
            <input
              class="lastname"
              v-model="lastName"
              type="text"
              name=""
              placeholder="Last name"
            />
            <input
              class="email"
              v-model="email"
              type="text"
              name=""
              placeholder="Mobile number or Email"
            />
            <input
              class="password"
              v-model="password"
              type="password"
              name=""
              placeholder="Password"
            />
            <p class="birthday">Birthday</p>
            <input class="birthday" v-model="dob" type="date" name="date" />
          </div>
          <br />
          <!-- <div class="radio">
              <input type="radio" id="radio01-01" name="demo01" /><label for="radio01-01">Male</label><br>
              <input type="radio" class="radio01-02" name="demo01" /><label for="radio01-02">Female</label><br>
              <input type="radio" id="radio01-03" name="demo01" /><label for="radio01-03">Other</label><br>
          </div> -->
          <select name="" id="">
            <option value="">Male</option>
            <option value="">Female</option>
          </select>
          <br>
          <button class="signup" @click="onsubmit">Sign Up</button>
        </form>
      </div>
    </center>
  </div>
</template>

<script scoped>
import axios from "axios";
export default {
  name: "registrationPage",
  data() {
    return {
      firstName: "",
      lastName: "",
      dob: "",
      email: "",
      password: "",
      picked: "",
    };
  },
  methods: {
    validate() {
      if (this.firstName === "") {
        alert("Please enter First Name");
        return false;
      }
      if (this.lastName === "") {
        alert("Please enter Last Name");
        return false;
      }
      if (this.dob === "") {
        alert("Please enter Date Of Birth");
        return false;
      }
      if (this.email === "") {
        alert("Please enter your email");
        return false;
      }
      if (this.password == "") {
        alert("Please enter your password");
        return false;
      }
      return true;
    },
    onsubmit() {
      const obj = {
        fname: this.firstName,
        lname: this.lastName,
        email: this.email,
        password: this.password,
        dob: this.dob,
        gender: this.picked,
      };
      if (this.validate()) {
        axios.post("link", obj).then((res) => {
          console.log(res);
          this.$router.push("/login");
        });
      }
    },
    created() {
      if (localStorage.getItem("sessionId") !== null) {
        this.$router.push("/login");
      }
    },
  },
};
</script>
<style scoped>
* {
  margin: 0;
  padding: 0;
}

.signup_body {
  font-family: arial;
  position: absolute;
  max-width: 500px;
  display: inline-block;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.signup_body .acc_crt {
  font-size: 40px;
  margin: 25px 0;
}
.signup_body .signup_form input {
  margin-top: 50px;
  height: 38px;
  width: 190px;
  padding-left: 10px;
  font-size: 18px;
  border: 1px solid silver;
  border-radius: 4px;
}
.signup_body .signup_form .lastname {
  margin-left: 15px;
}
.signup_body .signup_form .email,
.signup_body .signup_form .password,
.signup_body .signup_form .password2 {
  margin-top: 20px;
  width: 410px;
}
.signup_body .signup_form .birthday {
  margin-top: 15px;
  font-size: 20px;
  font-weight: bold;
  color: grey;
}
.signup_body .signup_form .birth_date {
  margin-top: 5px;
}
.signup_body .signup_form .month,
.signup_body .signup_form .day,
.signup_body .signup_form .year {
  height: 28px;
}
.signup_body .signup_form .day,
.signup_body .signup_form .year {
  margin-left: -5px;
}
.signup_body .signup_form .brth_hint {
  font-size: 11px;
  padding-left: 170px;
  margin-top: -28px;
  width: 150px;
}
.signup_body .signup_form a {
  text-decoration: none;
}
.signup_body .signup_form a:hover {
  text-decoration: underline;
}
.signup_body .signup_form input[type="radio"] {
  height: 15px;
  margin-left: -50px;
  margin-top: 10px;
}

.signup_body .signup_form .font {
  margin-left: 57px;
  margin-top: -17px;
}
.signup_body .signup_form .font2 {
  margin-left: 150px;
}
.signup_body .signup_form .signup {
  margin-top: 20px;
  height: 38px;
  width: 170px;
  color: white;
  font-size: 20px;
  font-weight: 600;
  border: 1px solid #006117;
  border-radius: 3px;
  cursor: pointer;
  outline: none;
  background: linear-gradient(#6fad5a, #66a150, #60974c);
}
.signup_body .signup_form .signup:hover {
  background: linear-gradient(#74b85e, #598b45);
}

.radio input[type="radio"] {
  line-height: 1.5;
  text-align: right;
  left:14px;
  right:15px;
  padding: 10px;


}
.radio01-01 {
  left: 18.67px;
  
}

.radio {
  display: flex;
  flex-direction: row;
}
</style>