<template>
  <section class="searchBox">
    <article>
      <button type="submit" class="searchButton"></button>
    </article>
    <article class="searchStr">
      <form action="" method="get">
        <input type="text" placeholder="Искать здесь...">
        <button type="reset" class="reset"></button>
      </form>
    </article>
  </section>
</template>

<style>
* {
  box-sizing: border-box;
}

form {
  position: absolute;
  width: 300px;
  margin: 0 auto;
}

input,
button {
  border: none;
  outline: none;
  border-radius: 4px;
}

input {
  width: 100%;
  height: 4.3vh;
  background: #343434;
  padding-left: 15px;
}

button {
  background: #343434;
  cursor: pointer;
}

.searchStr {
  position: absolute;
  left: 4.15vh;
  top: 15%;
}

.reset {
  position: absolute;
  top: 8px;
  right: 8px;
}

.reset::before {
  content: "╳";
}

.searchButton {
  position: absolute;
  height: 4.3vh;
  width: 4vh;
  margin-right: 8px;
  top: 0.05vh;
  border: 0 1px solid #ffffff;
  
}
</style>