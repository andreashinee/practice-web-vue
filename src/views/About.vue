<template>
  <div class="banner" @mouseover="showColor" @mouseout="showGrayscale">
  </div>
  <h1 class="banner-text">ABOUT US</h1>
  <div class="content">
    <p class="text-one">
      We are an English alternative rock band from Battle, East Sussex, formed in 1995. We met while at Tonbridge School together. Our band currently comprises Tom Chaplin (lead vocals, electric/acoustic guitar, piano), Tim Rice-Oxley (piano, synthesisers, bass guitar, backing vocals), Richard Hughes (drums, percussion, backing vocals), and Jesse Quin (bass guitar, acoustic/electric guitar, backing vocals). Our original line-up included founder and guitarist Dominic Scott, who left in 2001.
    </p>
    <p class="text-two">
      We achieved mainstream international success with the release of our debut album Hopes and Fears in 2004. Topping the UK chart, the album won the 2005 Brit Award for Best British Album and was the UK's second best-selling album of 2004. It is one of the best-selling albums in UK chart history. Our second album, Under the Iron Sea, released in 2006, topped the UK Albums Chart and debuted at number four on the US Billboard 200. Our third album Perfect Symmetry was released in October 2008 and our EP Night Train was released in May 2010. Our fourth studio album Strangeland was released in May 2012 and peaked at number one on the UK Albums Chart.
    </p>
    <p class="text-three">
      After the release of our compilation album The Best of Keane in 2013, we took a hiatus, lasting nearly five years. We returned after the hiatus with new music, announcing our fifth studio album titled Cause and Effect on 6 June 2019 and releasing the lead single from the album "The Way We Feel." A collection of the songs were written by Tim Rice-Oxley during his divorce, and after discussions with Tom who had visited Tim the previous year, we decided to proceed with recording the songs for the album. Cause and Effect was released on 20 September 2019. After the release of the album, we embarked on the Cause and Effect Tour, visiting Europe and Latin America, before the remainder of the tour was postponed due to the COVID-19 pandemic.
    </p>
    <p class="text-four">
      In May 2008, both Hopes and Fears (number 13) and Under the Iron Sea (number 8) were voted by readers of Q magazine as among the best British albums ever, with Keane, the Beatles, Oasis, and Radiohead the only artists having two albums in the top 20. In 2009, Hopes and Fears was listed as the ninth best-selling album of the 2000s decade in the UK. We are known for using keyboards as the lead instrument instead of guitar, differentiating us from most other rock bands. The inclusion of a distorted piano effect in 2006 and various synthesisers were a common feature in our music, which developed on the second and third albums. We have sold over 13 million records worldwide.
    </p>
  </div>
</template>

<style>
.banner {
  background-image: url('https://media.stubcloudstatic.com/stubhub-catalog/d_defaultLogo.jpg/t_f-fs-0fv,q_auto:low,f_auto,c_fill,$w_750_mul_3,$h_416_mul_3/performer/44713/d41d8cd98f00b204e9800998ecf8427e');
  background-size: cover;
  background-position: center -250px; 
  width: 100%;
  max-width: 100%;
  margin: 0 auto;
  height: 500px;
  display: flex;
  align-items: flex-end;
  transition: filter 0.5s;
  filter: grayscale(100%);
  cursor: pointer;
  margin-bottom: 50px;
  animation: fade-in 1s ease-in-out;
}

.banner:hover {
  filter: grayscale(0%);
}

.banner-text {
  font-family: 'Lora', serif;
  color: rgb(0, 0, 0);
  font-size: 24px;
  font-weight: normal; 
  margin: 0;
  text-align: center;
  animation: fade-in 2s ease-in-out;

}
.content {
  padding: 20px;
  max-width: 800px;
  margin: 0 auto;
  margin-top: 30px;
  margin-bottom: 50px;
}

.content p {
  font-size: 16px;
  line-height: 1.5;
  margin-bottom: 20px;
  
}

.text-one {
  animation: fade-in 3s ease-in-out;
}

.text-two {
  animation: fade-in 3.2s ease-in-out;
}

.text-three {
  animation: fade-in 3.4s ease-in-out;
}

.text-four {
  animation: fade-in 3.6s ease-in-out;
}



@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>

<script>
export default {
  methods: {
    showColor() {
      this.$refs.banner.style.filter = 'grayscale(0%)';
    },
    showGrayscale() {
      this.$refs.banner.style.filter = 'grayscale(100%)';
    },
  },
};
</script>
