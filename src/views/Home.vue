<template>
  <v-main>
    <v-parallax
      dark
      src="@/assets/top.jpeg"
    >
      <v-row align="center" justify="center">
        <v-col class="text-center" cols="12">
          <h1 class="display-1 font-weight-thin mb-4">MAMO_portfolio</h1>
          <!-- TODO: ここ差し替える -->
          <h4 class="subheading">平松守瑠</h4>
          <!-- ハッシュリンク追加 -->
          <a href="#works-header">works</a>
          <br /><a href="#about-header">about</a>
          <br /><a href="#contact-header">contact</a>
        </v-col>
      </v-row>
    </v-parallax>
    <v-container class="pb-16">
      <!-- ハッシュリンク追加 -->
      <h2 id="works-header" class="headline font-weight-bold text-center my-16">
        WORKS
      </h2>
      <section class="section">
        <ProductList></ProductList>
      </section>
<!-- 
       <h2 class="headline font-weight-bold text-center my-16">
        HOBBY
      </h2>
       <section class="section">
         <HobbyList></HobbyList>
      </section> -->



       <section class="section">
        <div class="inner">
          <div class="section-title-block">
            <h2 id="about-header" class="headline font-weight-bold text-center my-16">
              ABOUT
            </h2>
          </div>
          <v-row>
            <v-col cols="12" sm="12" md="4" lg="3"
              ><img
                src="@/assets/icon2.jpg"
                alt=""
                width="250"
            /></v-col>
            <v-col cols="12" sm="12" md="7" lg="9">
              <p class="text">
                分類:人間 高さ:1.68メートル 重さ:りんご170個分 性別:♂
                <br />
              </p>
            </v-col>
          </v-row>
        </div>
      </section>
       <!-- section class="section">
        <div class="inner">
          <div class="section-title-block">
            <h2 id="contact-header" class="headline font-weight-bold text-center my-16">
              CONTACT
            </h2>
            <p class="section-desc text-center">
              お問合わせは下記からご連絡をください。
            </p>
          </div>
          <div class="contact-wrapper">
            <div class="contact-list">
              <v-row class="text-center">
                <v-col>
                  <v-btn href="" x-large color="success" dark
                    >Extra large Button</v-btn
                  >
                </v-col>
              </v-row>
            </div>
          </div>
        </div>
      </section>  -->
    </v-container>
  </v-main>
</template>

<script>
import ProductList from "../components/ProductList.vue";
// import HobbyList from "../components/HobbyList.vue";
export default {
  name: "Home",
  components: { 
    ProductList,
    // HobbyList
  },
};
// import HobbyList from "../components/HobbyList.vue";
// export default {
//   name: "Home",
//   components: { HobbyList},
// };
</script>
