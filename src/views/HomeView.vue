<template>
    <div class="total">

        
        <div class="main1">
            <div class="main2">
                <div class="icon-main">
                    <div class="iconic1">
                        <img src="../assets/call.png" alt="">              
                    </div>
                    <div class="main-title">
                        <h1 class="h1">Give Us a Call</h1>
                        <p class="p1"> +91 098 098 8393</p>

                    </div>
                </div>
                <div class="icon-main">
                    <div class="iconic1">
                        <img src="../assets/email.png" alt="">              
                    </div>
                    <div class="main-title">
                        <h1 class="h1">Send Us an Email</h1>
                        <p class="p1">ecample@gmail.com</p>

                    </div>
                </div>

                <div class="icon-main">
                    <div class="iconic1">
                        <img src="../assets/location.png" alt="">              
                    </div>
                    <div class="main-title">
                        <h1 class="h1">Drop BY and Talk</h1>
                        <p class="p1">Unit 8012- 8014, Chandaka Industrial Estate, K I, I T University, Patia, Bhubaneswar, Odisha 751024</p>

                    </div>
                </div>


                <div class="insta">
                    <img src="../assets/twitter.png" alt="">
                    <img src="../assets/in.png" alt="">
                    <img src="../assets/insta.png" alt="">
                    <img src="../assets/facebook.png" alt="">
                </div>
            </div>
        </div>

        <div class="main_right">
          <div class="container">
            <div class="container_title">
              <p class="title_p">STAY IN CAONTACT</p>
              <h1 class="title_h">Get in Touch</h1>
            </div>
            <div class="container_box">
              <form action="#">
                <input class="box_inp" type="text" name="" v-model="info.name" id="" placeholder="Name">
                <input class="box_inp" type="text" name="" v-model="info.mobile" id="" placeholder="Mobile">
                <input class="box_inp" type="email" name="" v-model="info.email" id="" placeholder="Email">
                <textarea type="text" v-model="info.message" class="box_text" placeholder="Message"></textarea>
                <button class="box_btn" @click="check"><h2 class="h2">SUBMIT</h2></button>
              </form>
            </div>
          </div>
        </div>

    </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from "vue-router";
const val = ref(null);
const info = ref({
  name: "",
  mobile: "",
  email: "",
  message: "",
});
const route = useRouter();

const check = () => {
  console.log(info.value.name);
  if (info.value.name != "Ulugbek") {
    alert("Wrong name");
    return;
  }
  if (info.value.mobile != "+998917772597") {
    alert("Wrong mobile number");
    return;
  }
  if (info.value.email != "ulugbekyuldashboyev@gmail.com") {
    alert("Wrong email address");
    return;
  }

  route.push({ name: "about" });
};
</script>

<style lang="scss" scoped>
.total {
  width: 1920px;
  height: 1045px;
  display: flex;
  flex-direction: row;
}
.main1 {
  width: 845px;
  height: 1045px;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 259px 54px 260px 120px;
}

.main2 {
  width: 671px;
  display: inline-flex;
  height: 526px;
  padding: 10px;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  flex-shrink: 0;
}


.icon-main {
    width: 651px;
    height: 90px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 36px;
    align-self: stretch;
    
}
.iconic1 {
  width: 90px;
  height: 90px;
  display: flex;
  padding: 30px;
  align-items: flex-start;
  gap: 10px;
}

.main-title{
    width: 525px;
    height: 90px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    gap: 21px;
    flex: 1 0 0;
}

.h1{
    width: 218px;
    height: 42px;
    color: var(--foundation-painted-pony-normal-hover, #A78768);

/* Headingbold04 */
font-family: Encode Sans;
font-size: 35px;
font-style: normal;
font-weight: 600;
line-height: 120%; /* 42px */
}


.p1{
    width: 100%;
    color: var(--foundation-dark-dark-active, #0A0A0A);
font-family: Poppins;
font-size: 18px;
font-style: normal;
font-weight: 300;
line-height: normal;
text-transform: capitalize;

}
.insta{
    width: 651px;
    background-color: red($color: #000000);
    display: flex;
padding: 0px 1px;
align-items: center;
gap: 22px;
align-self: stretch;
margin-left: 20px;

}

.insta img{
    display: flex;
    flex-direction:row;
    align-items: flex-start;

    gap: 10px;
}

.main_right {
  width: 1075px;
  height: 1045px;
  flex-shrink: 0;
  background: var(--foundation-painted-pony-normal, #B99674);
  padding: 99px 162px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container{
  display: flex;
  width: 751px;
  height: 847px;
  padding: 35px 45px;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 64px;
  flex-shrink: 0;
  border-radius: 15px;
  background: var(--foundation-light-white, #FFF);
}

.container_title{
  width: 303px;
  height: 99px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}

.title_p{
  color: var(--foundation-painted-pony-darker, #413529);
  text-align: center;

  /* Paragraph01 */
  font-family: Encode Sans;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 25px; /* 138.889% */
}

.title_h{
  color: var(--foundation-painted-pony-darker, #413529);
  text-align: center;

  /* Heading02 */
  font-family: Encode Sans;
  font-size: 55px;
  font-style: normal;
  font-weight: 400;
  line-height: 120%; /* 66px */
}

.container_box{
  width: 684px;
  display: flex;
  height: 426px;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  flex-shrink: 0;
}


.box_inp{
  display: flex;
  width: 684px;
  padding: 20px;
  align-items: center;
  gap: 10px;
}

.box_text{
  display: flex;
  width: 684px;
  padding: 20px 20px 70px 20px;
  align-items: center;
  gap: 10px;
  resize: none;
 textarea::placeholder {
      color:#A7A7A7;
      font-family: Vollkorn;
      font-size: 17px;
      font-style: italic;
      font-weight: 400;
      line-height: 22px;
  }
}

.box_btn {
  display: flex;
  width: 725px;
  height: 68px;
  padding: 20px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  background: var(--foundation-painted-pony-normal-active, #94785D);
  // &:hover {
  //   border-radius: 15px;
  //   font-weight: 700;
  // }
}
.h2{
  color: var(--foundation-light-white, #FFF);
  text-align: center;

  /* Headingbold06 */
  font-family: Encode Sans;
  font-size: 23px;
  font-style: normal;
  font-weight: 600;
  line-height: 120%; /* 27.6px */
}

</style>