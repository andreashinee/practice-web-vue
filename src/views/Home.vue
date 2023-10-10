<template>
  <v-app>
    <div class="background-image">
      <h1 class="title">CELEBRATING 20 YEARS OF HOPES AND FEARS</h1>
      <a href="https://www.keanemusic.com/live/" class="button">View Tour Dates</a>
    </div>
  </v-app>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  overflow: hidden; /* Oculta el scroll vertical */
}

.button {
  font-family: 'Lora', serif;
  display: inline-block;
  background-color: #ffffff; 
  color: rgb(0, 0, 0);
  padding: 10px 20px;
  text-decoration: none;
  border-radius: 5px;
  font-size: 16px;
  margin-top: 20px;
}

.button:hover {
  background-color: #f3cfa7; 
}

.title {
  font-family: 'Lora', serif;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); 
}

.background-image {
  background-image: url('https://dynamicmedia.livenationinternational.com/e/u/j/ffd94804-6e8c-40ae-a8ff-ac2b6b4d0c47.jpg?auto=webp&width=1507.2');
  background-size: cover;
  background-attachment: fixed; 
  background-position: center center;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column; 
  justify-content: center;
  align-items: center;
  color: white; 
  filter: grayscale(100%); 
  transition: filter 0.7s;
  animation: fade-in 1s ease-in-out;
}

.background-image:hover {
  filter: grayscale(0%); 
}

@keyframes fadeIn {
  0% {
    opacity: 0; 
  }
  100% {
    opacity: 1; 
  }
}

.background-image::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0); 
  animation: fadeIn 1s ease-in-out; 
  z-index: -1; 
}
</style>
