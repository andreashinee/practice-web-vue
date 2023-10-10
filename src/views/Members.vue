<template>
  <div class="members">
    <div class="member">
      <div class="member-image" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 1</h2>
        <p>Descripción del Miembro 1.</p>
      </div>
    </div>
    
    <div class="member">
      <div class="member-image" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 2</h2>
        <p>Descripción del Miembro 2.</p>
      </div>
    </div>
    
    <div class="member">
      <div class="member-image" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 3</h2>
        <p>Descripción del Miembro 3.</p>
      </div>
    </div>
    
    <div class="member">
      <div class="member-image" @mouseover="showColor" @mouseout="showGrayscale"></div>
      <div class="member-text">
        <h2>Nombre del Miembro 4</h2>
        <p>Descripción del Miembro 4.</p>
      </div>
    </div>
  </div>
</template>

<style>
.members {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  padding: 20px;
}

.member {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.member-image {
  background-image: url('https://www.radiopop.cl/wp-content/uploads/2020/03/Ige-nADl_400x400.jpg');
  background-size: cover;
  background-position: center center;
  width: 200px;
  height: 200px;
  filter: grayscale(100%);
  cursor: pointer;
  transition: filter 0.5s;
}

.member-image:hover {
  filter: grayscale(0%);
}

.member-text {
  text-align: center;
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
