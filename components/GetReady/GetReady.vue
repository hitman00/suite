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
          <div :class="$style.download_image">
            <img src="@/assets/imgs/app_download.png" />
          </div>
          <div :class="$style.download_image">
            <img src="@/assets/imgs/google_play.png" />
          </div>
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
}

.download_image {
  position: relative;
  width: 40%;
  &:before {
    content: '';
    display: block;
    padding-bottom: 30%;
  }
  img {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    width: 100%;
    transition: all 0.3s ease;
    cursor: pointer;
    &:hover {
      opacity: 0.7;
    }
  }
}

@media (max-width: 1000px) {
  .title {
    font-size: 35px;
  }
}

@media (max-width: 800px) {
  .title {
    font-size: 25px;
  }

  .description {
    font-size: 16px;
  }
}

@media (max-width: 640px) {
  .max_size {
    flex-direction: column;
    padding-bottom: 5%;
    text-align: center;
  }

  .iphone_img {
    display: none;
  }

  .gt_boxs {
    width: 90%;
    margin: 0 auto;
  }

  .description {
    padding-right: 0;
  }

  .downloads {
    margin-right: 0;
  }
}

@media (max-width: 390px) {
  .title {
    font-size: 20px;
  }

  .description {
    font-size: 14px;
  }
}
</style>
