<template>
  <div class="mainCon">
    <UsersList />
    <aside class="asideCon">
      <h2>Sidebar</h2>
      <hr />
      <h3>What is this website?</h3>
      <h4>Awesome title 4</h4>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita
        explicabo vero commodi hic voluptates dignissimos non maxime, sunt enim
        architecto doloribus, minima nobis nemo. Numquam maiores aliquid itaque
        dolor aliquam!
      </p>
      <hr />
      <h4>Awesome title 4</h4>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Expedita
        explicabo vero commodi hic voluptates dignissimos non maxime, sunt enim
        architecto doloribus, minima nobis nemo. Numquam maiores aliquid itaque
        dolor aliquam!
      </p>
      <p>Random text to conclude.</p>
    </aside>
  </div>
</template>

<style>
.mainCon {
  display: flex;
  flex-direction: column-reverse;
  overflow: hidden;
}
.mainCon section p, .asideCon p {
    font-size: clamp(1rem, 2vw, 1.15rem);
}
@media (min-width: 650px) {
  .mainCon {
    flex-direction: row;
    align-items: flex-start;
    justify-content: space-around;
  }
  .mainCon section, .asideCon {
    width: 50%;
  }
}
</style>
