<template>
  <div class="header">
    <a href="https://vuejs.org/tutorial/#step-1"><span>Get Start with Vue.js The Progressive Framework...</span></a>
  </div>
  <div class="container">
    <h2>Declaring Reactive State</h2>
    <p>
      We can create a reactive object or array with the reactive() function:
      <code class="code-snippet">import { reactive } from 'vue'
          <br />
          const state = reactive({ count: 0 })
        </code>
      Reactive objects are JavaScript Proxies and behave just like normal
      objects. The difference is that Vue is able to track the property access
      and mutations of a reactive object.
    </p>
  </div>
  <div class="counter-container">
    <h2>Example</h2>
    <div class="counter">
      <button class="decrease" @click="decrease">-</button>
      <h2>{{ state.count }}</h2>
      <button class="increase" @click="increase">+</button>
    </div>
  </div>
  <footer class="footer">
    <p>Made with ❤️‍🔥 by Khashayar Shomali</p>
  </footer>
</template>

<script setup>
import { reactive } from "vue";

const state = reactive({ count: 0 });

const decrease = () => {
  state.count--;
};

const increase = () => {
  state.count++;
};
</script>

<style>
body {
  font-family: sans-serif;
  overflow-x: hidden;
  background-color: rgb(224, 255, 252);
  padding: 0;
  margin: 0;
}

.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.container p {
  width: 700px;
  text-align: center;
  line-height: 25px;
}

.code-snippet {
  height: 100px;
  background-color: rgb(33, 33, 33);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 20px 0;
}

.counter-container {
  margin-top: 20px;
  text-align: center;
}

.counter-container h2 {
  font-size: 42px;
}

.counter {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 50px;
}

.increase {
  padding: 5px 10px;
  background-color: rgb(183, 255, 237);
  border-radius: 9px;
  cursor: pointer;
  border: none;
  font-size: 22px;
}

.decrease {
  padding: 5px 12px;
  background-color: rgb(255, 212, 183);
  border-radius: 9px;
  cursor: pointer;
  border: none;
  font-size: 22px;
}

.increase:hover {
  background-color: rgb(93, 255, 215);
}

.decrease:hover {
  background-color: rgb(253, 185, 140);
}

.header {
  height: 50px;
  background-color: aquamarine;
  margin-bottom: 20px;
  font-size: 14px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: sticky;
  top: 0;
}

.header a {
  color: rgb(18, 18, 18);
  text-decoration: none;
}

.footer {
  height: 120px;
  background-color: aquamarine;
  font-size: 14px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: sticky;
  bottom: 0;
}

/* Mobile Screens */

@media screen and (max-width: 480px) {
  .container {
    padding: 20px 0px;
  }

  .container h2 {
    font-size: 18px;
  }

  .container p {
    width: 300px;
  }

  .increase {
    padding: 5px 10px;
    font-size: 32px;
  }

  .decrease {
    padding: 5px 14px;
    font-size: 32px;
  }

  .counter-container h2 {
    font-size: 28px;
  }

  .header {
    font-size: 12px;
  }

  .footer {
    font-size: 14px;
  }
}
</style>
