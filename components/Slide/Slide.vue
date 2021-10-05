<template>
  <div :class="$style.slide_main">
    <div v-for="(i, id) in list" :key="id" :class="$style.slide_box">
      <div :class="[$style.text_box, id == 1 ? $style.fix_box : '']">
        <div :class="$style.slide_tag">{{ i.tag }}</div>
        <div :class="$style.slide_title">{{ i.title }}</div>
        <div :class="$style.slide_description">{{ i.description }}</div>
      </div>
      <div :class="$style.slide_img"><img :src="i.img" /></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slide',
  data() {
    return {
      list: [
        {
          tag: 'CONTROL ANALYTICS',
          title: 'Empowering Control Analytics Engagement',
          description:
            'Reach your audience with the right message at the right time. Discover users that are ready for an upsell.',
          img: require('@/assets/imgs/curly0.png'),
        },
        {
          tag: 'PARTNERSHIP',
          title: 'Connect With Suite Real Assistant',
          description:
            'Reach your audience with the right message at the right time. Discover users that are ready for an upsell.',
          img: require('@/assets/imgs/curly10.png'),
        },
      ],
    }
  },
}
</script>

<style lang="scss" module>
.slide_main {
  width: 70%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  padding-bottom: 13%;
}

.slide_box {
  margin-top: 6%;
  width: 46%;
}

.text_box {
  padding-right: 7%;

  &.fix_box {
    margin-top: 10%;
  }
}

.slide_tag {
  font-weight: 600;
  color: #296ade;
}

.slide_title {
  color: #162d59;
  font-size: 35px;
  font-weight: 700;
  margin: 3% 0;
}

.slide_description {
  font-weight: 300;
}

.slide_img {
  position: relative;
  margin-top: 5%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 76%;
  }
  img {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    top: 0;
    width: 100%;
  }
}

@media (max-width: 1000px) {
  .slide_title {
    font-size: 25px;
  }

  .slide_description {
    font-size: 14px;
  }
}

@media (max-width: 775px) {
  .slide_tag {
    font-size: 14px;
  }

  .slide_title {
    font-size: 20px;
  }
}

@media (max-width: 600px) {
  .slide_main {
    flex-direction: column;
  }

  .slide_box {
    width: 100%;
  }
}
</style>
