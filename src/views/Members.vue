<template>
  <div class="centered-container">
    <div class="members">
      <div class="member" @click="toggleText(1)">
        <div class="member-image one" @mouseover="showColor" @mouseout="showGrayscale"></div>
        <div class="member-text" v-show="showText[1]">
        <h2>Tom Chaplin</h2>
          <p>Full Name: Thomas Oliver Chaplin</p>
          <p>Date of Birth: March 8, 1979</p>
          <p>Role in the band: Tom Chaplin is the lead vocalist of Keane. His distinctive voice is a fundamental part of the band's sound. </p>
          <p>Additional Info: Before joining Keane, Tom attended Sherborne School and met Tim Rice-Oxley and Richard Hughes during his time at the University of East Sussex. His emotive vocal performance has been a hallmark of many of Keane's songs.</p>
      </div>
    </div>
    
    <div class="member" @click="toggleText(2)">
      <div class="member-text" v-show="showText[2]">
        <h2>Tim Rice Oxley</h2>
          <p>Full Name: Timothy James Rice-Oxley</p>
          <p>Date of Birth: June 2, 1976</p>
          <p>Role in the band: Tim Rice-Oxley is the keyboardist and primary songwriter for Keane. He is responsible for writing most of the band's songs.</p>
          <p>Additional Info: Tim and Tom met in school and founded the band along with Richard Hughes. His ability to compose emotive melodies and his keyboard skills have been instrumental in Keane's success.</p>
      </div>
      <div class="member-image two" @mouseover="showColor" @mouseout="showGrayscale"></div>
    </div>
    
    <div class="member" @click="toggleText(3)">
      <div class="member-image three" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text" v-show="showText[3]">
        <h2>Richard Hughes</h2>
          <p>Full Name: Richard David Hughes</p>
          <p>Date of Birth: September 8, 1975</p>
          <p>Role in the band: Richard Hughes is the drummer for Keane and provides the rhythmic foundation for the band's music.</p>
          <p>Additional Info: Richard joined the band after it was originally formed as a quartet. His drumming style has been essential to Keane's distinctive sound, and his contribution to the band is highly valued.</p>
      </div>
    </div>
    
    <div class="member"  @click="toggleText(4)">
      <div class="member-text" v-show="showText[4]">
        <h2>Jesse Quin</h2>
        <p>Full Name: Jesse Thomas Quin</p>
        <p>Date of Birth: March 3, 1979</p>
        <p>Jesse Quin joined Keane as a touring bassist in 2007 and continued to perform with the band for several years. He also contributed to their 2010 EP "Night Train." His addition to the band's live performances added depth to their sound, and he became a valued member of the Keane team during his tenure.</p>
      </div>
      <div class="member-image four" @mouseover="showColor" @mouseout="showGrayscale"></div>
    </div>
  </div>
</div>
</template>

<style>

.centered-container {
  display: flex;
  height: 80vh; 
  justify-content: center; 
}

.members {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  padding: 20px;
}


.member {
  justify-content: center; 
  align-items: center; 
  display: flex;
  flex-direction: row;
  align-items: center;
}

.member-image {
  background-size: cover;
  background-position: center center;
  width: 200px;
  height: 200px;
  filter: grayscale(100%);
  cursor: pointer;
  transition: filter 0.5s;
  margin-left: 50px;
  margin-right: 50px;
}



.one {
  background-image: url('https://www.radiopop.cl/wp-content/uploads/2020/03/Ige-nADl_400x400.jpg');
}

.two {
  background-image: url('https://www.sodajerker.com/wp-content/uploads/2019/11/timriceoxley.jpg');
}

.three {
  background-image: url('https://i.pinimg.com/originals/54/3b/73/543b73959365dc86192c5a58685ae044.jpg');
}

.four {
  background-image: url('https://media.licdn.com/dms/image/C4E03AQGOtrK2wCRmWw/profile-displayphoto-shrink_800_800/0/1646757882186?e=2147483647&v=beta&t=ytR9yD69hZ-hCegrLqqmBzoyze8FXAHuJWOFUe3dtjQ');
}


.member-image:hover {
  filter: grayscale(0%);
}

.member-text {
  margin: 0; 
  padding: 0; 
  

}

.member-text h2 {
  font-family: 'Lora', serif;
  font-size: 24px;
  margin: 0; 
}

.member-text p {
  font-size: 16px;
  margin: 0; 
  
}
</style>

<script>
export default {
  data() {
    return {
      showText: {
        1: false,
        2: false,
        3: false,
        4: false,
      },
    };
  },
  methods: {
    toggleText(member) {
      this.showText[member] = !this.showText[member];
    },
    showColor(event) {
      event.currentTarget.style.filter = 'grayscale(0%)';
    },
    showGrayscale(event) {
      event.currentTarget.style.filter = 'grayscale(100%)';
    },
  },
};
</script>
