<script setup>
import { ref } from "vue";

const isDropdownOpen = ref(false);

const toggleDropdown = () => {
  isDropdownOpen.value = !isDropdownOpen.value;
};
</script>

<template>
  <body>
    <div class="container">
      <div class="header">
        <div class="logo">
          <h1>NETSOL</h1>
        </div>
        <div class="dropdown">
          <button class="dropbtn">Regions</button>
          <div class="dropdown-content">
            <NuxtLink to="/en-us">USA</NuxtLink>
            <NuxtLink to="/en-uk">UK</NuxtLink>
            <NuxtLink to="/en-cn">China</NuxtLink>
            <NuxtLink to="/en-pk">Pakistan</NuxtLink>
          </div>
        </div>
      </div>
      <div class="Text">
        <h2 class="heading">Latest Insights from Leading Voices</h2>
        <p class="description">
          Solving the world’s problems through technology wouldn’t be possible
          without our most important invention: the NetSol. Have a look at our
          talented teams.
        </p>
      </div>
      <div class="viewAll">View All News</div>
      <div class="cardContainer">
        <div class="card-list">
          <div class="card-item">
            <img src="./../assets/1.png" alt="Card Image" />
            <span class="blogType">News</span>
            <p class="title">Leasing Life Conference & Awards</p>
            <p class="blogDescription">
              Solving the world’s problems through technology wouldn’t be
              possible without our most important invention.
            </p>
          </div>
          <div class="card-item">
            <img src="./../assets/2.png" alt="Card Image" />
            <span class="blogType">Blog</span>
            <p class="title">Auto Finance Summit 2023</p>
            <p class="blogDescription">
              Solving the world’s problems through technology wouldn’t be
              possible without our most important invention.
            </p>
          </div>
          <div class="card-item">
            <img src="./../assets/3.png" alt="Card Image" />
            <span class="blogType">News</span>
            <p class="title">Careers at Netsol</p>
            <p class="blogDescription">
              Solving the world’s problems through technology wouldn’t be
              possible without our most important invention.
            </p>
          </div>
          <div class="card-item">
            <img src="./../assets/4.png" alt="Card Image" />
            <span class="blogType">Blog</span>
            <p class="title">Leasing Life Conference & Awards</p>
            <p class="blogDescription">
              Solving the world’s problems through technology wouldn’t be
              possible without our most important invention.
            </p>
          </div>
        </div>
      </div>
    </div>
  </body>
</template>

<style scoped>
body {
  background-image: url("./../assets/background.png");
}
.header {
  height: 83px;
  top: 16px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

h1 {
  width: 90px;
  height: 16px;
  top: 33px;
  left: 92px;
  color: azure;
}

button {
  width: 177px;
  height: 40px;
  top: 21px;
  left: 1651px;
  border-radius: 100px;
  color: white;
  border: 1px solid;
  background: radial-gradient(
      163.75% 163.75% at 23.45% 140%,
      #0025ce 0%,
      rgba(9, 93, 230, 0.53) 100%
    ),
    linear-gradient(
      180deg,
      rgba(255, 255, 255, 0.46) 0%,
      rgba(255, 255, 255, 0) 100%
    );
}

.Picture {
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 30px;
}

.cardPicture {
  width: 1200px;
}

.heading {
  margin-top: 15px;
  font-family: Aeonik;
  font-size: 56px;
  font-weight: 500;
  line-height: 67px;
  letter-spacing: 0em;
  text-align: center;
  color: #ffff;
}

.description {
  margin-left: 106px;
  margin-right: 106px;
  font-family: Aeonik;
  font-size: 24px;
  font-weight: 400;
  line-height: 32px;
  letter-spacing: 0em;
  text-align: center;
  color: #ffff;
}
.viewAll {
  font-family: Aeonik;
  font-size: 16px;
  font-weight: 500;
  line-height: 24px;
  letter-spacing: 0em;
  text-align: center;
  color: #ffff;
}
.list {
  height: 20px;
  color: white;
  font-weight: 500px;
}
.cardContainer {
  object-fit: contain;
}

.card-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  max-width: 1250px;
  padding: 20px;
  gap: 10px;
}
.card-list .card-item {
  padding: 26px;
  border-radius: 8px;
  list-style: none;
  cursor: pointer;
  text-decoration: none;
  border: 2px solid transparent;
  transition: border 0.5s ease;
}
.title {
  height: 30px;
  font-family: Aeonik;
  font-size: 16px;
  font-weight: 500;
  line-height: 30px;
  letter-spacing: 0em;
  text-align: left;
  color: white;
}

.blogDescription {
  font-family: Aeonik;
  font-size: 14px;
  font-weight: 200;
  text-align: left;

  color: white;
}
.card-list .card-item img {
  width: 100%;
  aspect-ratio: 16/9;
  border-radius: 8px;
  object-fit: cover;
}
.card-list span {
  display: inline-block;
  background: #f7dff5;
  margin-top: 32px;
  padding: 8px 15px;
  font-size: 0.75rem;
  border-radius: 50px;
  font-weight: 600;
}
.card-list .blogType {
  background-color: rgba(255, 255, 255, 0.1);

  color: rgba(24, 235, 254, 1);
}

.dropbtn {
  background-color: #4caf50;
  color: white;
  padding: 16px;
  font-size: 16px;
  border: none;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
}

.dropdown {
  position: relative;
  display: inline-block;
}

.dropdown-content {
  display: none;
  position: absolute;
  background-color: linear-gradient(0deg, #092530, #092530),
    linear-gradient(0deg, #ffffff, #ffffff);
  min-width: 160px;
  box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
  z-index: 1;
}

.dropdown-content a {
  color: white;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {
  background-color: #f1f1f1;
}

.dropdown:hover .dropdown-content {
  display: block;
}

.dropdown:hover .dropbtn {
  background-color: #3e8e41;
}

.card-list .editor {
  background-color: #d6f8d6;
  color: #205c20;
}
.card-item h3 {
  color: #000;
  font-size: 1.438rem;
  margin-top: 28px;
  font-weight: 600;
}
.card-item .arrow {
  display: flex;
  align-items: center;
  justify-content: center;
  transform: rotate(-35deg);
  height: 40px;
  width: 40px;
  color: #000;
  border: 1px solid #000;
  border-radius: 50%;
  margin-top: 40px;
  transition: 0.2s ease;
}
.card-list .card-item:hover .arrow {
  background: #000;
  color: #fff;
}
@media (max-width: 1200px) {
  .card-list .card-item {
    padding: 15px;
  }
}
@media screen and (max-width: 980px) {
  .card-list {
    margin: 0 auto;
  }
}
</style>
