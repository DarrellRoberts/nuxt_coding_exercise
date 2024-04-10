<template>
  <nav>
    Navigation
    <ul class="navbarCon">
      <li><a href="/">Home</a></li>
      <li><a href="/">Home 2</a></li>
      <li><a href="/">Home 3</a></li>
      <li><a href="/">Home 4</a></li>
      <li><a href="/">Home 5</a></li>
      <li><a href="/">Home 6</a></li>
      <li><a href="/">Home 7</a></li>
      <li><a href="/">Home 8</a></li>
      <li><a href="/">Home 9</a></li>
    </ul>
  </nav>
</template>

<style>
.navbarCon {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  justify-items: center;	
  padding: 0px;
  margin: 0px;
  list-style: none;
  overflow: hidden;
}
.navbarCon li {
  margin: 0.5rem 0rem;
  font-size: clamp(1rem, 2.25vw, 1.3rem);
}

@media (min-width: 1200px) {
  .navbarCon {
   display: flex;
   justify-content: space-evenly;
   align-items: center;
  }
}
</style>
