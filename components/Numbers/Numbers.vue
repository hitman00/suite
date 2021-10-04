<template>
  <div :class="$style.number_main">
    <div
      v-observe-visibility="{
        callback: visibilityChanged,
        throttle: 500,
      }"
      :class="$style.numbers_boxs"
    >
      <div
        v-for="(i, id) in list"
        :key="id"
        :class="[$style.box, id == 1 ? $style.add_border : '']"
      >
        <div :class="$style.title">{{ i.title }}</div>
        <div :class="$style.number">{{ i.num }}{{ i.number }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Number',
  data: () => ({
    hover: 0,
    num: 0,
    percent: 0,
    list: [
      {
        title: 'Engagement User',
        number: '% per week',
        num: 0,
      },
      {
        title: 'User Transactions',
        number: '+ Billion',
        num: 0,
      },
      {
        title: 'User Approved Fast',
        number: ' hovers',
        num: 0,
      },
    ],
  }),

  methods: {
    visibilityChanged(isVisible) {
      if (isVisible) {
        this.show = true
        this.animation_number()
      }
    },
    animation_number() {
      const clock = setInterval(() => {
        this.list[0].num++
        if (this.list[0].num >= 124) {
          clearInterval(clock)
        }
      }, 30)
      const per = setInterval(() => {
        this.list[1].num++
        if (this.list[1].num >= 80) {
          clearInterval(per)
        }
      }, 40)
      const number = setInterval(() => {
        this.list[2].num++
        if (this.list[2].num++ >= 16) {
          clearInterval(number)
        }
      }, 100)
    },
  },
}
</script>

<style lang="scss" module>
.number_main {
  width: 85%;
  background: #f8fafb;
  float: right;
}

.numbers_boxs {
  display: flex;
  justify-content: space-evenly;
}

.box {
  padding: 0% 6%;
  margin: 4% 0;
  width: 33%;
  &.add_border {
    border-right: 2px solid #e8eef2;
    border-left: 2px solid #e8eef2;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

.title {
  font-size: 18px;
  color: #a9b0c0;
  padding-bottom: 10%;
}

.number {
  font-weight: 600;
  font-size: 35px;
  color: #162d59;
}
</style>
