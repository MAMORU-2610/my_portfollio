<template>
  <div>
    <v-row>
      <product
        v-for="(product, key) in filterdList"
        :key="key"
        :product="product"
      >
      </product
    ></v-row>
  </div>
</template>

<script>
import Product from './Product.vue';
export default {
  name: 'ProductList',
  components: { Product },
  data: () => ({
    sortYear: '全て',
    products: [
      {
        id: 1,
        name: 'Projection Mapping',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/project.jpg'),
        year: '2022',
        category: 'project',
        use: 'processing/reacTIVition',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'https://www.meisei-u.ac.jp/2022/2022021401.html'
        ],
      },
      {
        id: 2,
        name: 'LEDcube[Getting Ready]',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/big.png'),
        year: '2022',
        category: 'project',
        use: 'Arduino',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://google.com'
        ],
      },
      {
        id: 7,
        name: 'Augmented Reality',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/AR.jpeg'),
        year: '2022',
        category: 'hobby',
        use: 'swift',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://google.com'
        ],
      },
      {
        id: 3,
        name: 'num1',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num1.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://openprocessing.org/sketch/1574873'
        ],
      },
      {
        id: 4,
        name: 'num2',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num2.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://openprocessing.org/sketch/1574875'
        ],
      },
      {
        id: 5,
        name: 'num3',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num3.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://openprocessing.org/sketch/1574876'
        ],
      },
      {
        id: 3,
        name: 'num4',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num4.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'https://openprocessing.org/sketch/1586819'
        ],
      },
      {
        id: 3,
        name: 'num5',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num5.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'https://openprocessing.org/sketch/1586820'
        ],
      },
      {
        id: 3,
        name: 'num6',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/num6.png'),
        year: '2022',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'https://openprocessing.org/sketch/1586823'
        ],
      },
      {
        id: 6,
        name: 'tanpopo',
        // TODO: ここに差し替えたい画像のパスを入れてね
        image: require('@/assets/tanpopo.png'),
        year: '2021',
        category: 'hobby',
        use: 'processing',
        urls: [
          // TODO: ここにリンクしたいURLを入れてね
          'http://openprocessing.org/sketch/1368457'
        ],
      },
      
      // image: "vue-portfolio/src/assets/re-vr.png",
      // {
      //   id: 2,
      //   name: "work2",
      //   image: "https://dummyimage.com/250x150/000/fff",
      //   year: "2019",
      //   category: "LP",
      //   use: "Vue.js",
      // },
      // {
      //   id: 3,
      //   name: "work3",
      //   image: "https://dummyimage.com/250x150/000/fff",
      //   year: "2018",
      //   category: "ECサイト",
      //   use: "デザイン",
      // },
      // {
      //   id: 4,
      //   name: "work4",
      //   image: "https://dummyimage.com/250x150/000/fff",
      //   year: "2019",
      //   category: "LP",
      //   use: "Vue.js",
      // },
    ],
  }),
  computed: {
    filterdList: function() {
      const newList = [];
      for (let i = 0; i < this.products.length; i++) {
        if (this.sortYear === "2020" && this.products[i].year === "2020") {
          newList.push(this.products[i]);
        } else if (
          this.sortYear === "2019" &&
          this.products[i].year === "2019"
        ) {
          newList.push(this.products[i]);
        } else if (
          this.sortYear === "2018" &&
          this.products[i].year === "2018"
        ) {
          newList.push(this.products[i]);
        } else if (this.sortYear === "全て") {
          newList.push(this.products[i]);
        }
      }
      return newList;
    },
  },
  methods: {
    sortYearChanged: function(year) {
      console.log(year);
      this.sortYear = year;
    },
  },
};
</script>
