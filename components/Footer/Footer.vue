<template>
  <div :class="$style.footer_main">
    <div :class="$style.max_size">
      <div :class="$style.footer_box">
        <div :class="$style.logo">
          <div :class="$style.logo_img">
            <img src="@/assets/imgs/logo1.png" />
          </div>
          Suite
        </div>
        <div :class="$style.copy_right">
          Copyright 2021 Suite Company Allright Reserved
        </div>
        <div :class="$style.social">
          <img src="@/assets/imgs/linkedin.png" />
          <img src="@/assets/imgs/facebook.png" />
          <img src="@/assets/imgs/tweeter.png" />
        </div>
      </div>
      <div :class="$style.footer_box">
        <div :class="$style.page_box">
          <div v-for="(i, id) in list" :key="id">
            <div :class="$style.title">{{ i.title }}</div>
            <div v-for="page in i.pages" :key="page.id" :class="$style.pages">
              {{ page }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  data: () => ({
    list: [
      {
        title: 'Menu',
        pages: ['Home', 'Features', 'Customer', 'About us'],
      },
      {
        title: 'Company',
        pages: ['Management', 'Our Story ', 'Career', 'Partnership'],
      },
      {
        title: 'Support',
        pages: [
          'Support Center',
          'Transaction',
          'Privacy Policy',
          'Contact us',
        ],
      },
    ],
  }),
}
</script>

<style lang="scss" module>
.footer_main {
  background: #f9f9f9;
}

.max_size {
  max-width: 1230px;
  padding-left: 15px;
  padding-right: 15px;
  margin: 0 auto;
  display: flex;
  padding-top: 6%;
  padding-bottom: 6%;
}

.footer_box {
  width: 50%;
}

.logo {
  display: flex;
  color: #162d59;
  font-weight: 600;
  font-size: 35px;
  align-items: end;
}

.logo_img {
  position: relative;
  width: 12%;
  margin-right: 2%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 100%;
  }
  img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
  }
}

.copy_right {
  margin: 6% 50% 4% 0;
  color: #4f4e4ec7;
  font-weight: 500;
}

.social {
  display: flex;
  justify-content: space-between;
  margin-right: 70%;
  img {
    width: 15%;
    display: block;
  }
}

.page_box {
  display: flex;
  justify-content: space-between;
}

.title {
  font-weight: 600;
  color: #162d59;
  font-size: 22px;
}

.pages {
  color: #4f4e4ec7;
  font-weight: 500;
  font-size: 15px;
  line-height: 3;
  cursor: pointer;
  transition: all 0.3s ease;
  &:hover {
    opacity: 0.7;
  }
}
</style>
