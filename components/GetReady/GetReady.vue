<template>
  <div :class="$style.main">
    <div :class="$style.max_size">
      <div :class="$style.gt_boxs">
        <div :class="$style.iphone_img">
          <img src="@/assets/imgs/iphone2.png" />
        </div>
      </div>
      <div :class="$style.gt_boxs">
        <div :class="$style.title">Get Ready To Join Suite?</div>
        <div :class="$style.description">
          Lets enjoy with Suits various previleges and attractive offers for you
        </div>
        <div :class="$style.downloads">
          <img src="@/assets/imgs/app_download.png" />
          <img src="@/assets/imgs/google_play.png" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'GetReady',
}
</script>

<style lang="scss" module>
.main {
  background: #10153d;
}

.max_size {
  max-width: 1230px;
  padding: 0 15px;
  margin: 0 auto;
  display: flex;
}

.gt_boxs {
  width: 50%;
  color: #fff;
}

.iphone_img {
  position: relative;
  margin: -20% auto 0;
  width: 80%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 125%;
  }
  img {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
  }
}

.title {
  font-size: 50px;
  font-weight: 600;
  margin: 10% 0 3%;
}

.description {
  font-size: 18px;
  padding-right: 35%;
  color: #ffffffc9;
}

.downloads {
  display: flex;
  justify-content: space-evenly;
  margin-top: 8%;
  margin-right: 13%;
  img {
    width: 40%;
    transition: all 0.3s ease;
    cursor: pointer;
    &:hover {
      opacity: 0.7;
    }
  }
}
</style>
