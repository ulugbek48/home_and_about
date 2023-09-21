<template>
    <div class="container">

        <div class="right">
            <div class="right_box">
                <div class="right_title">
                    <p class="title_p">STAY IN CAONTACT</p>
                    <h1 class="title_h">Get in Touch</h1>
                </div>
                <div class="right_boxes">
                    <div class="inp">
                        <input class="name" v-model="info.name" type="text" name="" id="" placeholder="Name" required>
                        <input class="phone" type="text" name="" id="" placeholder="Phone No." v-model="info.mobile" required>
                    </div>
                    <input class="email" type="email" name="" id="" placeholder="Email I'd" v-model="info.email" required>
                    <input class="proj" type="text" name="" id="" placeholder="Project Brief..." v-model="info.message" required>
                    <div class="inp_2">
                        <input class="chbox" type="checkbox" name="" id="">
                        <label class="label" for="">Subscribe Newslatter</label>
                    </div>
                    <button class="btn_box" type="submit"><span  class="span">Send Message</span></button>
                </div>
            </div>
        </div>

        <div class="left">
            <img src="../assets/phone_email_sms.png" alt="">
        </div>
    </div>
</template>

<script setup>

import { ref } from "vue";
import { useRouter } from "vue-router";
const val = ref(null);
const info = ref({
  name: "",
  mobile: "",
  email: "",
  message: "",
});
const route = useRouter();

const check = (e) => {
  e.preventDefault();

  route.push({ name: "cars" });
};
</script>

<style lang="scss" scoped>

.container{
    width: 1920px;
    display: inline-flex;
    flex-direction: row;
    height: 1045px;
    padding-left: 0px;
    justify-content: flex-end;
    align-items: center;
    gap: 138px;
}

.right{
    width: 986px;
    height: 1045px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
}

.right_box {
    width: 712px;
    height: 797px;
    display: flex;
    padding: 75px;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.right_title{
    width: 303px;
    height: 98px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 13px;
    margin-right: 100px;
}

.title_p{
    color: #000;
    text-align: center;

    /* Body03 */
    font-family: Inter;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 120%; /* 19.2px */
}

.title_h{
    color: #000;
    text-align: center;

    /* Heading02 */
    font-family: Encode Sans;
    font-size: 55px;
    font-style: normal;
    font-weight: 400;
    line-height: 120%; /* 66px */
}

.right_boxes{
    width: 562px;
    display: flex;
    height: 508px;
    flex-direction: column;
    align-items: center;
    gap: 47px;
    align-self: stretch;
}

.inp{
    width: 576px;
    height: 63px;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    gap: 25px;
    align-self: stretch;
    margin-right: 10px;
}

.name{
    width: 271px;
    display: flex;
    height: 63.396px;
    padding: 10px 5px;
    align-items: center;
    gap: 10px;
    flex: 1 0 0;
}

.phone{
    width: 271px;
    display: flex;
    height: 63.396px;
    padding: 10px 5px;
    align-items: center;
    gap: 10px;
    flex: 1 0 0;
}

.email{
    width: 562px;
    display: flex;
    height: 63.396px;
    padding: 10px 5px;
    align-items: center;
    gap: 10px;
    align-self: stretch;
}

.proj{
    width: 562px;
    display: flex;
    height: 63px;
    padding: 10px 5px;
    align-items: center;
    gap: 10px;
    align-self: stretch;
}


.inp_2{
    width: 562px;
    height: 40px;
    display: flex;
    padding: 10px;
    align-items: flex-start;
    gap: 10px;
    align-self: stretch;
}

.label{
    width: 139px;
    height: 17px;
    color: var(--foundation-dark-normal, #5C5C5C);
    text-align: center;

    /* Paragraphbold02 */
    font-family: Encode Sans;
    font-size: 14px;
    font-style: normal;
    font-weight: 600;
    line-height: 120%; /* 16.8px */
}

.chbox{
    width: 20px;
    height: 20px; 
    border: 1px solid #FFF;
    background: var(--foundation-light-normal-active, #EEECE7);
    box-shadow: 0px 2px 2px 0px rgba(0, 0, 0, 0.10);   
}

.btn_box{
    width: 562px;
    display: flex;
    height: 75.849px;
    padding: 10px 23px;
    justify-content: center;
    align-items: center;
    gap: 10px;
    flex-shrink: 0;
    align-self: stretch;
    border-radius: 8px;
    border: 0.5px solid #C4C4C4;
    background: var(--foundation-dark-normal, #5C5C5C);
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.04);
}

.span{
    width: 140px;
    height: 24px;
    color: #FFF;
    text-align: center;

    /* Body02 */
    font-family: Inter;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 120%; /* 24px */
}
.left img{
    width: 934px;
    height: 1045px;
}

</style>