<template>
  <div class="members">
    <div class="member">
      <div class="member-image one" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 1</h2>
        <p>Descripción del Miembro 1.</p>
      </div>
    </div>
    
    <div class="member">
      <div class="member-text">
        <h2>Nombre del Miembro 2</h2>
        <p>Descripción del Miembro 2.</p>
      </div>
      <div class="member-image two" @mouseover="showColor" @mouseout="showGrayscale"></div>
    </div>
    
    <div class="member">
      <div class="member-image three" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 3</h2>
        <p>Descripción del Miembro 3.</p>
      </div>
    </div>
    
    <div class="member">
      <div class="member-text ">
        <h2>Nombre del Miembro 4</h2>
        <p>Descripción del Miembro 4.</p>
      </div>
      <div class="member-image four" @mouseover="showColor" @mouseout="showGrayscale"></div>
    </div>
  </div>
</template>

<style>
.members {
  display: grid;
  grid-template-columns: 1fr;
  gap: 20px;
  padding: 20px;
}

.member {
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
  text-align: center;
  flex: 1; /* Para que el texto ocupe todo el espacio restante */
}

.member-text h2 {
  font-family: 'Lora', serif;
  font-size: 24px;
  margin: 10px 0;
}

.member-text p {
  font-size: 16px;
  margin: 0;
}
</style>

<script>
export default {
  methods: {
    showColor(event) {
      event.currentTarget.style.filter = 'grayscale(0%)';
    },
    showGrayscale(event) {
      event.currentTarget.style.filter = 'grayscale(100%)';
    },
  },
};
</script>
