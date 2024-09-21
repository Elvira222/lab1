<template>
  <div class="main">
    <header class="header">
      <nav class="nav">
        <ul class="nav__list">
          <li class="nav__item"><a href="#home">Home</a></li>
          <li class="nav__item"><a href="#cats">Cats</a></li>
          <li class="nav__item"><a href="#cute">Cute Cats</a></li>
          <li class="nav__item"><a href="#funny">Funny Cats</a></li>
          <li class="nav__item"><a href="#videos">Cat Videos</a></li>
          <li class="nav__item"><a href="#adoption">Adopt a Cat</a></li>
        </ul>
        <div class="nav__search">
          <input type="text" placeholder="Search for cats..." />
          <button class="search__button">
            <i class="fa fa-search"></i>
          </button>
        </div>
      </nav>
    </header>
    <div class="container">
      <div class="main__card">
        <div class="card card--small card--top-left">
          <img src="./assets/black.jpg" alt="Cute Kitten" />
          <div class="card-content">
            <h3>Cute Kittens Playing</h3>
            <p>These playful kittens love to chase each other around!</p>
            
          </div>
        </div>

        <div class="card card--small card--bottom-left">
          <img src="./assets/brown.jpg" alt="Adorable Fluffy Cat" />
          <div class="card-content">
            <h3>Adorable Fluffy Cat</h3>
            <p>This fluffy friend enjoys lounging in the sun.</p>
            
          </div>
        </div>

        <div class="card card--large">
          <img src="./assets/ginger.jpg" alt="The Cutest Cat" />
          <div class="card-content">
            <h3>The Cutest Cats of 2023</h3>
            <p>A collection of this year's most adorable cats!</p>
            
          </div>
        </div>

        <div class="card card--small card--top-right">
          <img src="./assets/gray.jpg" alt="Funny Cat Faces" />
          <div class="card-content">
            <h3>Funny Cat Faces</h3>
            <p>These cats have the funniest expressions you'll ever see!</p>
           
          </div>
        </div>

        <div class="card card--small card--bottom-right">
          <img src="./assets/white.jpg" alt="White kitten" />
          <div class="card-content">
            <h3>White Kitten</h3>
            <p>Nothing is cuter than sleeping kittens!</p>
           
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>

<style lang="scss">
.header {
  background-color: #f8f9fa;
  padding: 1rem;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.nav {
  display: flex;
  align-items: center;
}
.nav__list {
  list-style: none;
  display: flex;
  margin: 0;
  padding: 0;
}
.nav__item {
  margin: 0 1rem;
}
.nav__item a {
  text-decoration: none;
  color: black;
}
.nav__search {
  display: flex;
  align-items: center;
  margin-left: 1rem;
}
.nav__search input {
  padding: 0.5rem;
  border: 1px solid #ced4da;
  border-radius: 4px;
}
.search__button {
  background-color: transparent;
  border: none;
  cursor: pointer;
  margin-left: 0.5rem;
}
.search__button .fa-search {
  font-size: 1rem;
  color: black;
}

.main__card {
  cursor: pointer;
  margin-top: 100px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: auto auto;
  gap: 20px;
  padding: 20px;
  position: relative;
}

.card {
  position: relative;
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  width: 100%;
}

.card img {
  object-fit: cover;
  width: 100%;
  height: 100%;
  display: block;
}
.card::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0) 80%,
    rgba(0, 0, 0, 0.7) 100%
  );
}

.card-content {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  color: white;
  padding: 15px;
  padding-bottom: 5px;
  text-align: left;
  background-color: rgba(0, 0, 0, 0.6); /* Added background for better readability */
}

.card h3 {
  margin-bottom: 10px;
  font-size: 18px;
}

.card p {
  font-size: 14px;
  opacity: 0.9; /* Adjusted opacity for better visibility */
}

.card--large {
  grid-column: 2 / 3;
  grid-row: 1 / 3;
}

.card--small {
  height: 100%;
}

.card--top-left {
  grid-column: 1 / 2;
  grid-row: 1 / 2;
}

.card--bottom-left {
  grid-column: 1 / 2;
  grid-row: 2 / 3;
}

.card--top-right {
  grid-row: 1 / 2;
}

.card--bottom-right {
  grid-row: 2 / 3;
}
</style>

