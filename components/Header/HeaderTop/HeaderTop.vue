<template>
  <div :class="$style.headertop_main">
    <div :class="$style.cycle">
      <div :class="$style.cycle2"></div>
    </div>
    <div :class="$style.boxs">
      <div :class="$style.logo">Suite.</div>
      <div :class="$style.meno">
        <ul>
          <li>Features</li>
          <li>Customers</li>
          <li>Products</li>
          <li>Resources</li>
          <li>Blog</li>
        </ul>
      </div>
      <div :class="$style.login">
        <ul>
          <li>Login</li>
          <li><a href="#">Github</a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderTop',
}
</script>

<style lang="scss" module>
.headertop_main {
  color: #162d59;
}

.cycle {
  width: 57%;
  background: linear-gradient(
    0deg,
    rgba(240, 244, 246, 1) 0%,
    rgba(241, 247, 250, 1) 53%,
    rgba(254, 254, 254, 1) 100%
  );
  border-radius: 50%;
  position: absolute;
  padding-bottom: 54%;
  top: -38%;
  left: -10%;
}

.cycle2 {
  width: 29%;
  background: #edf0f6;
  border-radius: 50%;
  position: absolute;
  padding-bottom: 27%;
  top: 41%;
  left: 38%;
}

.boxs {
  display: flex;
  align-items: center;
  padding: 2% 0;
  position: relative;
}

.logo {
  width: 10%;
  font-weight: 900;
  font-size: 30px;
}

.meno {
  width: 70%;
}

.login {
  width: 20%;

  ul {
    display: flex;
    justify-content: space-between;
    li {
      padding: 5% 10%;
      transition: all 0.4s ease;
      border-radius: 10px;
      cursor: pointer;
      font-weight: 500;
      a {
        color: #162d59;
      }
      &:hover {
        background: #367df9;
        color: #fff;
      }
    }
  }
}

.meno {
  ul {
    display: flex;
    li {
      padding: 1.5% 3%;
      transition: all 0.4s ease;
      border-radius: 10px;
      cursor: pointer;

      &:hover {
        background: #367df9;
        color: #fff;
      }
    }
  }
}
</style>
