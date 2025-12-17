<template>
  <div class="container">
    <div class="content-card">
      <h1>This About Page</h1>
      <p>Ini adalah Animasi-slider.app sederhana dengan menggunakan CSS-animation,JavaScript, Vite, dan Framework Vuejs-3</p>
      <hr />
      <span>
        Copy Paste &copy;<a href="https://www.instagram.com/mr.sahfikri/">Koding Sebelum Tidur</a>
      </span>
    </div>
  </div>
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 90vh;
  padding: 40px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f8f9fa;
  border-radius: 12px;
}

.content-card {
  text-align: center;
  max-width: 600px;
  padding: 2rem;
  background: #ffffff;
  border-radius: 16px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease;
}

.content-card:hover {
  transform: translateY(-5px);
}

/* Styling Judul */
h1 {
  color: #2c3e50;
  font-size: 2.5rem;
  margin-bottom: 1rem;
  position: relative;
  display: inline-block;
}

h1::after {
  content: '';
  display: block;
  width: 50px;
  height: 4px;
  background: #42b883;
  margin: 8px auto 0;
  border-radius: 2px;
}

p {
  color: #636e72;
  font-size: 1.1rem;
  line-height: 1.6;
  margin: 15px;
}

span {
  color: #636e72;
  font-size: 1.1rem;
  line-height: 4.5vh;
}

span a {
  text-decoration: none;
  color: #636e72;
}

span a:hover {
  color: #42b883;
}

span a:visited {
  color: #660092;
}
</style>
