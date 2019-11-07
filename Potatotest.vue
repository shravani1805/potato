<template>
  <div class="maindiv">
    <!-- this is blue box container -->
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" class="bg1">
          <u class="para">This is the page for potato voting</u>
        </b-col>

        <!-- this is thumb container -->
        <b-col sm="6" class="bg2">
          <p class="para">Made by with Love By [Name]</p>
        </b-col>
      </b-row>
    </b-container>

    <!-- this is likes  container -->

    <b-container class="cart-bg">
      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img
                src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/mashedPotato.jpg"
                width="150"
                height="90"
              />
            </b-nav-item>
            <b-nav-item>
              <b-button @click="likefnc+=1" variant="success">Like</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">likes: {{likefnc}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>

      <!-- this is likes  container  -->

      <b-row>
        <b-col sm="6" offset="4" class="potato-banner">
          <b-nav>
            <b-nav-item>
              <img
              src="https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/bakedPotato.jpeg"
                width="150"
                height="90"
              />
            </b-nav-item>
            <b-nav-item>
              <b-button @click="dislikefnc+=1" variant="danger">Dislike</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">dislikes: {{dislikefnc}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>

      <!-- 
      this is reset  container-->
      <b-row>
        <b-col sm="6" offset="5" class="potato-banner1">
          <b-nav>
            <b-nav-item>
              <b-button @click="reset" variant="warning">Reset</b-button>
            </b-nav-item>
            <b-nav-item disabled>
              <span class="text">Total : {{likefnc + dislikefnc}}</span>
            </b-nav-item>
          </b-nav>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>
<script>
export default {
  data() {
    return {
      likefnc: 0,
      dislikefnc: 0
    };
  },
  methods: {
    reset() {
      (this.likefnc = 0), (this.dislikefnc = 0);
    }
  }
};
</script>
<style  scoped>
.maindiv {
  width: 90%;
  margin: 0 auto;
}
.bg1 {
  background-image: url("https://previews.123rf.com/images/gabe123/gabe1231502/gabe123150200007/36355527-hailstones-texture-on-blue-colour-background.jpg");
  height: 40vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.bg2 {
  background-image: url("https://raw.githubusercontent.com/cognitedata/fe-interview-challenge-vue/master/resources/thumbs.png");
  height: 40vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
}
.cart-bg {
  background-image: url("http://images.unsplash.com/photo-1533134486753-c833f0ed4866?ixlib=rb-1.2.1&q=80&fm=jpg&crop=entropy&cs=tinysrgb&w=1080&fit=max");
  height: 55vh;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.potato-banner {
  padding: 20px;
}
.text {
  color: white;
}
.para {
  position: absolute;
  top: 100px;
  left: 60px;
  font-size: 30px;
}
</style>