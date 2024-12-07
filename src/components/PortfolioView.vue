<template>
  <div class="text-center mt-4">
    <h2>Our Project</h2>
    <div style="width: 120px; margin: 0 auto">
      <v-slider v-model="slider2" color="red" label="track-color"></v-slider>
    </div>
    <div class="first" id="project">
      <v-row>
        <v-col cols="12">
          <div class="child">
            <v-btn icon="fas fa-laptop" color="red" class="text-white"></v-btn>
            <h3 class="ml-3 mt-4">Web Design</h3>
            <p class="text-grey ml-3 mt-4 text-caption">
              Lorem, ipsum dolor sit amet <br />consectetur adipisicing
              <br />consectetur adipis
            </p>
          </div>
          <div class="child">
            <v-btn icon="fas fa-mobile-alt" color="red" class="text-white"></v-btn>
            <h3 class="ml-3 mt-4">App Design</h3>
            <p class="text-grey ml-3 mt-4 text-caption">
              Lorem, ipsum dolor sit amet <br />consectetur adipisicing
              <br />consectetur adipis
            </p>
          </div>
          <div class="child">
            <v-btn icon="fas fa-camera" color="red" class="text-white"></v-btn>
            <h3 class="ml-3 mt-4">Photography</h3>
            <p class="text-grey ml-3 mt-4 text-caption">
              Lorem, ipsum dolor sit amet <br />consectetur adipisicing
              <br />consectetur adipis
            </p>
          </div>
        </v-col>
      </v-row>
      <v-divider></v-divider>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {
      slider2: 50,
    };
  }
}
</script>

<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 200px;
  width: 100%;
  color: white;
}

.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}

.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}


.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>