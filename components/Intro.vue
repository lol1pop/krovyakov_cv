<template>
  <div class="container">
    <div class="intro">
      <div class="intro__info">
        <div class="info__column info__column_left">
            <span class="text-content">
              <span class="info__name">I,m Denis Krovyakov</span>
              <br>
              <span class="info__time">25/8</span>
              <span class="info__position">
                <vue-typed-js :strings="['BackEnd dev']" :cursorChar="'_'" :startDelay="1000">
                  <span class="typing"></span>
                </vue-typed-js>
              </span>
            </span>
          <div class="info__about"></div>
        </div>
        <div class="info__column info__column_right">
          <div class="info__photo"></div>
        </div>
      </div>
      <div class="intro__download">
        <div class="text-block">
          <span class="text-content">Обновлено {{ afterDays }} дней назад</span>
        </div>
        <a class="button_download text-content" href="static/favicon.ico" download> download CV </a>
      </div>
    </div>
  </div>
</template>

<script>
import Vue from 'vue';
import { daysHavePassed } from '~/utils/utils'

export default Vue.extend({
  name: 'Intro',
  data() {
    return { }
  },
  computed: {
    afterDays() {
      return Math.trunc(daysHavePassed(this.$store.state.intro.dataUpdate))
    }
  }
})
</script>

<style scoped lang="scss">
@import "assets/css/colors";
@import "assets/css/mixin";

.intro {
  position: relative;
  display: flex;
  align-items: center;
  
/*  height: 100%;
  min-height: 100vh;*/
}

.intro__info {
  min-height: 330px;
  margin-top: 170px;
  margin-bottom: 160px;
}

.text-content {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  
  .info__name {
    font-size: 50px;
    text-transform: uppercase;
    font-weight: 400;
  }
  
  .info__time {
    font-size: 100px;
    font-weight: 700;
  }
  
  .info__position {
    font-size: 35px;
    font-weight: 700;
    line-height: 30%;
  }
}

.intro__download {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  align-items: center;
  
  position: absolute;
  bottom: 24px;
  left: 0;
  
  margin-left: 16px;
  margin-right: 16px;
  
  .text-block {
    max-width: 100%;
    flex-basis: auto;
    font-size: 13px;
    line-height: 150%;
    letter-spacing: .02em;
  }
}

.button_download {
  width: 163px;
  height: 29px;
  left: 32px;
  top: 93px;
  
  background: $D-dark-gray;
  border-radius: 6px;
  
  margin-left: 16px;
  margin-right: 16px;
  
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  padding: 6px 8px;
  
  text-decoration: none;
}

a.button_download:hover {
  @include box-shadow(0px 0px 10px 0px $D-dark-purple);
}

.info__about {
  min-width: 600px;
  min-height: 300px;
  background-image: url(static/carbon.png);
  background-size: cover;
  background-position: left;
  margin-left: -16px;
  margin-top: 16px;
}
</style>