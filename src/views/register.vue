<template>
 <div>
      <center>
  <div class="signup_body">
    <p class="acc_crt">Sign up with QuinBook</p>
    <p class="free_hint">It's free and always will be.</p>
    <form class="signup_form">
      <div>
        <input class="firstname" type="text" name="" placeholder="First name">
        <input class="lastname" type="text" name="" placeholder="Last name">
        <input class="email" type="text" name="" placeholder="Mobile number or Email">
        <input class="password" type="password" name="" placeholder="Password">
      </div>
      <p class="birthday">Birthday</p>
      <div class="birth_date">
       <select class="month">
         <option>Month</option><option>Jan</option><option>Feb</option><option>Mar</option>
         <option>Apr</option><option>May</option><option>Jun</option><option>Jul</option>
         <option>Aug</option><option>Sep</option><option>Oct</option><option>Nov</option>
         <option>Dec</option>
       </select>
       <select class="day">
         <option>Day</option><option>1</option><option>2</option><option>3</option>
         <option>4</option><option>5</option><option>6</option><option>7</option>
         <option>8</option><option>9</option><option>10</option><option>11</option>
         <option>12</option><option>13</option><option>14</option><option>15</option>
         <option>16</option><option>17</option><option>18</option><option>19</option>
         <option>20</option><option>21</option><option>22</option><option>23</option>
         <option>24</option><option>25</option><option>26</option><option>27</option>
         <option>28</option><option>29</option><option>30</option>
       </select>
       <select class="year">
         <option>Year</option><option>1970</option><option>1972</option><option>1974</option>
         <option>1976</option><option>1978</option><option>1980</option><option>1982</option>
         <option>1984</option><option>1986</option><option>1988</option><option>1990</option>
         <option>1992</option><option>1995</option><option>1997</option><option>2000</option>
         <option>2002</option><option>2003</option><option>2004</option><option>2005</option>
         <option>2006</option><option>2007</option><option>2008</option>
       </select>
      </div>
      <br>
      <br>

      <div class="radio">
  <label><input type="radio" name="gender" value="male"> Male</label>
  <label><input type="radio" name="gender" value="female"> Female</label>
  <label><input type="radio" name="gender" value="other"> Prefer Not to Say</label>
 </div>
      <button class="signup">Sign Up</button>
      
    </form>
  </div>
      </center>
  </div> 
  
</template>

<script>
export default {

}
</script>

<style scoped>

*{
    margin: 0;
    padding: 0;
}

.signup_body{
    font-family: arial;
    position: absolute;
    max-width: 500px;
    display: inline-block;
    left:50%;
    top:50%;
    transform: translate(-50%,-50%);
}
.signup_body .acc_crt{
    font-size: 40px;
    margin: 25px 0;
}
.signup_body .signup_form input{
    margin-top: 50px;
    height: 38px;
    width: 190px;
    padding-left: 10px;
    font-size: 18px;
    border: 1px solid silver;
    border-radius: 4px;
}
.signup_body .signup_form .lastname{
    margin-left: 15px;
}
.signup_body .signup_form .email,
.signup_body .signup_form .password,
.signup_body .signup_form .password2{
    margin-top: 20px;
    width: 410px;
}
.signup_body .signup_form .birthday{
    margin-top: 15px;
    font-size: 20px;
    font-weight: bold;
    color: grey;
}
.signup_body .signup_form .birth_date{
    margin-top: 5px;
}
.signup_body .signup_form .month,
.signup_body .signup_form .day,
.signup_body .signup_form .year{
    height: 28px;
}
.signup_body .signup_form .day,
.signup_body .signup_form .year{
    margin-left: -5px;
}
.signup_body .signup_form .brth_hint{
    font-size: 11px;
    padding-left: 170px;
    margin-top: -28px;
    width: 150px;
}
.signup_body .signup_form a{
    text-decoration: none;
}
.signup_body .signup_form a:hover{
    text-decoration: underline;
}
.signup_body .signup_form input[type="radio"]{
    height: 15px;
    margin-left: -50px;
    margin-top: 30px;
}
.signup_body .signup_form input[value="female"]{
    margin-left: -100px;
}
.signup_body .signup_form .font{
    margin-left: 57px;
    margin-top: -17px;
}
.signup_body .signup_form .font2{
    margin-left: 150px;
}
.signup_body .signup_form .signup{
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
    background: linear-gradient(#6fad5a, #66a150, #60974C);
}
.signup_body .signup_form .signup:hover{
    background: linear-gradient(#74b85e, #598B45);
}

.radio input[type='radio'] {
  display: none; /*removes original button*/
 }
    
.signup_body .radio label:before { /*styles outer circle*/
    content: " ";
    display: inline-block;
    position: relative;
    top: 5px;
    margin: 0 5px 0 0;
    width: 10px;
    height: 10px;
    border-radius: 11px;
    border: 2px solid orange;
    background-color: transparent;
}

.signup_body .radio label input[type='radio']:checked + label:after { /*styles inside circle*/
    border-radius: 11px;
    width: 5px;
    height: 5px;
    position: absolute;
    top: 5px;
    left: 5x;
    content: " ";
    display: block;
    background-color: blue;
}
</style>