<template>
  <v-app id="home">
    <NavBar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative; margin-top: 120px;">
              <h1 class="text-grey">Hello</h1>
              <h1 class="text-white">Welcome to Noodles would</h1>
              <span class="text-grey">You can order any noodles here</span><br />
              <v-btn tile dark class="text-yellow mt-8" variant="outlined">Order</v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="position: absolute;z-index: 9999;bottom:0;margin-left: auto;margin-right: auto;left: 0;right: 0;text-align: center;"></div>
              <v-icon>fas fa-angle-double-down</v-icon>
          </v-col>
          <v-col cols="5">
            <div style="position: relative;z-index: 9999;" class="mt-16">
              <v-img src="noodles.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="Recipe.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About Noodles</h5>
              <h4 class="mt-2">We all love to eat noodles</h4>
              <h4>in this world</h4>
              <p class="text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, minus magnam temporibus perferendis eligendi aliquam, sapiente quaerat ut blanditiis quam sequi ea! Et accusantium tenetur dolorem ipsam at temporibus voluptates?</p>
              <br />
              <p class="text-grey">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum, minus magnam temporibus perferendis eligendi aliquam, sapiente quaerat ut blanditiis quam sequi ea! Et accusantium tenetur dolorem ipsam at temporibus voluptates?</p>
              <v-btn tile dark color="yellow" class="mt-4">Download Menu</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="mt-4" id="services">
        <v-divider></v-divider>
        <div class="d-flex justify-center mt-16 mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Taiwan</v-btn>
          <v-btn class="mr-2" variant="tonal">Japan</v-btn>
          <v-btn class="mr-2" variant="tonal">Korea</v-btn>
          <v-btn variant="tonal">India</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{isHovering, props}">
                <v-card :elevation="isHovering ? 12: 2" :class="{'on-hover' : isHovering}" v-bind="props">
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="mt-16" id="news">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="news1.jpeg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Lily | 04 Mar 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatibus rem eveniet culpa repudiandae voluptatum fugit quis ipsum quas in, incidunt nihil quasi, quam earum ab dolor iusto ut optio officiis.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="news2.jpeg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Lily | 04 Mar 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatibus rem eveniet culpa repudiandae voluptatum fugit quis ipsum quas in, incidunt nihil quasi, quam earum ab dolor iusto ut optio officiis.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mw-auto" max-width="344" height="">
                <v-img src="news3.jpeg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>
                  By Lily | 04 Mar 2023
                </v-card-subtitle>
                <v-card-text>
                  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptatibus rem eveniet culpa repudiandae voluptatum fugit quis ipsum quas in, incidunt nihil quasi, quam earum ab dolor iusto ut optio officiis.
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from 'vue';

// Components
import NavBar from '@/components/NavBar.vue';
import FooterView from '@/components/FooterView.vue';

export default defineComponent({
  name: 'HomeView',
  setup(){
    return {
      slider2:50,

      items:[
        {
          img: "noodles1.jpeg",
        },
        {
          img: "noodles2.jpeg",
        },
        {
          img: "noodles3.jpeg",
        },
        {
          img: "noodles4.jpeg",
        },
        {
          img: "noodles5.jpeg",
        },
        {
          img: "noodles6.jpeg",
        },
      ],
    }
  },

  components: {

    NavBar,
    FooterView,
  },
});
</script>

<style scoped>
.v-container{
  padding: 16px 0;
}
.head{
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 500px;
  width: 100%;
  color: white;
}
.head:before{
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  /* transform: skew(0deg, 6deg); */
}
.head:after{
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  /* transform: skew(0deg, -6deg); */
}
.egg{
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #FBDF7E;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
.first{
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}
.child{
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.imgHover{
  padding: 0 200px;
}
.pre{
  width: 100%;
  height: 430px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}
.hire{
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>