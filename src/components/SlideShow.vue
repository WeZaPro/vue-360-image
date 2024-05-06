<template>
  <v-container fill-height>
    <v-row justify="center" align="center">
      <v-col cols="12" sm="0">
        <!-- <div class="center image-container"> -->
        <div>
          <!-- <v-img
            :width="600"
            aspect-ratio="16/9"
            cover
            :src="imgChangeA"
          ></v-img> -->
          <v-app id="inspire">
            <v-main>
              <v-container>
                <v-card>
                  <v-card-text>
                    <v-img
                      max-width="1200"
                      max-heigth="1200"
                      :src="imgChangeA"
                    ></v-img>
                    <div class="center text-center">
                      <span
                        class="text-h2 font-weight-light"
                        v-text="bpm"
                      ></span>
                    </div>

                    <div class="slide-container">
                      <v-slider
                        v-model="bpm"
                        :color="color"
                        :step="1"
                        max="52"
                        min="0"
                        track-color="grey"
                      ></v-slider>
                    </div>
                  </v-card-text>
                </v-card>
              </v-container>
            </v-main>
          </v-app>
        </div>
        <!-- <div class="center">
          <span class="text-h2 font-weight-light" v-text="bpm"></span>
        </div> -->
        <!-- <div class="slide-container">
          <v-slider
            v-model="bpm"
            :color="color"
            :step="1"
            max="52"
            min="0"
            track-color="grey"
          ></v-slider>
        </div> -->
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    img: '',
    imgLocation: '',
    bpm: 0,
    imgId: 0,
    isPlaying: false,
  }),
  mounted() {
    // console.log(' this.changeImg()', this.changeImg());
    // this.changeImg();
  },

  computed: {
    imgChangeA() {
      console.log('this.bpm ', this.bpm);
      if (this.bpm < this.bpm + 1) return `../../public/img_${this.bpm}.jpg`;
    },
    imgChange() {
      if (this.bpm < 2) return `../../public/img_0.jpg`;
      if (this.bpm < 4) return `../../public/img_1.jpg`;
      if (this.bpm < 6) return `../../public/img_2.jpg`;
      if (this.bpm < 8) return `../../public/img_3.jpg`;
      if (this.bpm < 10) return `../../public/img_4.jpg`;
      if (this.bpm < 12) return `../../public/img_5.jpg`;
      if (this.bpm < 14) return `../../public/img_6.jpg`;
      if (this.bpm < 16) return `../../public/img_7.jpg`;
      if (this.bpm < 18) return `../../public/img_8.jpg`;
      if (this.bpm < 20) return `../../public/img_9.jpg`;
      if (this.bpm < 22) return `../../public/img_10.jpg`;
      if (this.bpm < 24) return `../../public/img_11.jpg`;
      if (this.bpm < 26) return `../../public/img_12.jpg`;
      if (this.bpm < 28) return `../../public/img_13.jpg`;
      if (this.bpm < 30) return `../../public/img_14.jpg`;
      if (this.bpm < 32) return `../../public/img_15.jpg`;
      if (this.bpm < 34) return `../../public/img_16.jpg`;
      if (this.bpm < 36) return `../../public/img_17.jpg`;
      if (this.bpm < 38) return `../../public/img_18.jpg`;
      if (this.bpm < 40) return `../../public/img_19.jpg`;
      if (this.bpm < 42) return `../../public/img_20.jpg`;
      if (this.bpm < 44) return `../../public/img_21.jpg`;
      if (this.bpm < 46) return `../../public/img_22.jpg`;
      if (this.bpm < 48) return `../../public/img_23.jpg`;
      if (this.bpm < 50) return `../../public/img_24.jpg`;
      if (this.bpm < 52) return `../../public/img_25.jpg`;
      if (this.bpm < 54) return `../../public/img_26.jpg`;
      if (this.bpm < 56) return `../../public/img_27.jpg`;
      if (this.bpm < 58) return `../../public/img_28.jpg`;
      if (this.bpm < 60) return `../../public/img_29.jpg`;
      if (this.bpm < 62) return `../../public/img_30.jpg`;
      if (this.bpm < 64) return `../../public/img_31.jpg`;
      if (this.bpm < 68) return `../../public/img_32.jpg`;
      if (this.bpm < 70) return `../../public/img_33.jpg`;

      if (this.bpm < 72) return `../../public/img_34.jpg`;
      if (this.bpm < 74) return `../../public/img_35.jpg`;
      if (this.bpm < 76) return `../../public/img_36.jpg`;
      if (this.bpm < 78) return `../../public/img_37.jpg`;
      if (this.bpm < 80) return `../../public/img_38.jpg`;
      if (this.bpm < 82) return `../../public/img_39.jpg`;
      if (this.bpm < 84) return `../../public/img_40.jpg`;
      if (this.bpm < 86) return `../../public/img_41.jpg`;
      if (this.bpm < 88) return `../../public/img_42.jpg`;
      if (this.bpm < 90) return `../../public/img_43.jpg`;
      if (this.bpm < 92) return `../../public/img_44.jpg`;
      if (this.bpm < 94) return `../../public/img_45.jpg`;
      if (this.bpm < 96) return `../../public/img_46.jpg`;
      if (this.bpm < 98) return `../../public/img_47.jpg`;
      if (this.bpm < 100) return `../../public/img_48.jpg`;
      if (this.bpm < 102) return `../../public/img_49.jpg`;
      if (this.bpm < 104) return `../../public/img_50.jpg`;
      if (this.bpm < 106) return `../../public/img_51.jpg`;
      if (this.bpm < 108) return `../../public/img_52.jpg`;
    },
    color() {
      if (this.bpm < 10) return 'indigo';
      if (this.bpm < 20) return 'teal';
      if (this.bpm < 30) return 'green';
      if (this.bpm < 40) return 'orange';
      return 'red';
    },
    animationDuration() {
      return `${60 / this.bpm}s`;
    },
  },

  methods: {
    changeImg() {
      this.imgLocation = `../../public/imgB/img_${this.imgId}.png`;

      console.log('this.imgLocation -> ', this.imgLocation);
      return this.imgLocation;
    },
    decrement() {
      this.bpm--;
    },
    increment() {
      this.bpm++;
    },
    toggle() {
      this.isPlaying = !this.isPlaying;
    },
  },
};
</script>

<style scoped>
#app {
  width: 100%;
  margin: 0 auto;
  padding: 0;
  text-align: center;
}
.center {
  margin: auto;
  width: 50%;
  border: 0px solid green;
  padding: 10px;
}
.container {
  height: 300px;
  width: 645px;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 2px solid black;
}
</style>
