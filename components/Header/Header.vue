<template>
  <div :class="$style.main">
    <div :class="$style.max_size">
      <!-- <div :class="$style.cycle">
        <span></span>
      </div> -->

      <HeaderTop />
      <div :class="$style.slid_box">
        <div :class="$style.boxs">
          <div :class="$style.fix_size">
            <div :class="$style.title">
              Deliver Big Impact in Product Marketing
            </div>
            <div :class="$style.description">
              The easiest way for conversions analytics & engagement product
              analytics to help more users in one place
            </div>
            <div :class="$style.search">
              <input type="email" placeholder="Your email address" />
              <div :class="$style.btn">Get Started</div>
            </div>
            <div :class="$style.description">
              "We'll respect the inbox and never share your email
            </div>
            Partnership by
            <div :class="$style.shop">
              <div v-for="(i, id) in images" :key="id" :class="$style.shop_img">
                <img :src="i" />
              </div>
            </div>
          </div>
        </div>
        <div :class="$style.boxs">
          <div :class="$style.bck_cycle"></div>
          <div :class="$style.women_image">
            <img src="@/assets/imgs/women4.png" alt="" />
          </div>
          <div :class="$style.note">
            <div :class="$style.note_logo">
              <img src="@/assets/imgs/nestle.png" alt="" />
            </div>
            <div :class="$style.note_title">Nestle.</div>
            <div :class="$style.note_description">Partners Suite.</div>
            <div :class="$style.note_title"><span>+80%</span> Sales Rate</div>
            <div :class="$style.note_description">
              Track which aspects of your product keep & build users retained
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderTop from './HeaderTop/HeaderTop.vue'
export default {
  name: 'Header',
  components: {
    HeaderTop,
  },
  data: () => ({
    images: [
      require('@/assets/imgs/Shopify-Logo.png'),
      require('@/assets/imgs/PayPal.png'),
      require('@/assets/imgs/Forbes.png'),
    ],
  }),
}
</script>

<style lang="scss" module>
.main {
  width: 100%;
  background: #edf0f6;
  position: relative;
}

.max_size {
  max-width: 1230px;
  padding: 0 15px;
  margin: 0 auto;
}

.cycle {
  width: 40%;
  padding-bottom: 40%;
  background: #fefefe;
  border-radius: 50%;
  position: absolute;
  top: -10%;
  left: -6%;
  span {
    display: block;
    width: 40%;
    padding-bottom: 40%;
    background: #edf0f6;
    border-radius: 50%;
    top: 21%;
    position: absolute;
    left: 32%;
  }
}

.slid_box {
  display: flex;
  overflow: hidden;
}

.boxs {
  width: 50%;
  position: relative;
}

.fix_size {
  margin-top: 7%;
  margin-left: 11%;
}

.title {
  font-weight: 700;
  font-size: 50px;
  line-height: 1.4;
  color: #162d59;
}

.description {
  font-weight: 200;
  margin: 6% 16% 6% 0;
}

.search {
  padding: 1.5%;
  display: flex;
  justify-content: space-between;
  border-radius: 10px;
  background: #fff;
  margin-right: 10%;
  input {
    width: 60%;
    background: none;
    border: 0;
    margin-left: 2%;
    font-size: 18px;
    &:focus {
      outline: none;
    }
  }
}

.btn {
  color: #fff;
  font-weight: 500;
  background: #367df9;
  padding: 3% 5%;
  border-radius: 10px;
  transition: all 0.3s ease;
  cursor: pointer;
  &:hover {
    opacity: 0.8;
  }
}

.shop {
  display: flex;
  justify-content: space-between;
  margin: 6% 0;
}

.shop_img {
  position: relative;
  width: 25%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 30%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
}

.bck_cycle {
  display: block;
  width: 100%;
  padding-bottom: 100%;
  background: #fff;
  border-radius: 50%;
  position: absolute;
  top: 12%;
}

.women_image {
  position: absolute;
  width: 85%;
  right: 8%;
  bottom: 0;
  &:before {
    content: '';
    display: block;
    padding-bottom: 119%;
  }
  img {
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
  }
}

.note {
  background: linear-gradient(
    0deg,
    #b9b5b5bf 0%,
    #c7c7c796 53%,
    #ffffff6e 100%
  );
  box-shadow: 0 8px 32px 0 rgba(20, 18, 18, 0.7);
  border-radius: 30px;
  border: 1px solid rgba(255, 255, 255, 0.18);
  position: absolute;
  top: 50%;
  color: #fff;
  padding: 0 4% 4%;
  margin: 0 25%;
  span {
    color: #f4bb1a;
  }
}

.note_logo {
  background: #2464a9;
  border-radius: 50%;
  border: 5px solid #fff;
  position: absolute;
  width: 26%;
  right: 10%;
  top: -19%;
  img {
    padding: 21%;
    display: block;
    width: 100%;
  }
}

.note_title {
  font-weight: 600;
  font-size: 18px;
  margin-top: 7%;
}
</style>
