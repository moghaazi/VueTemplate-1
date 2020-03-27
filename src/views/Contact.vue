<template>
  <div class="container">
    <WelcomeMessage />
    <form>
      <input type="text" placeholder="Name" />
      <input type="email" placeholder="Email" />
      <input type="password" placeholder="Password" />
      <button>Send</button>
      <img width="800" src="../assets/images/sign-in.svg" />
    </form>
  </div>
</template>

<script>
import WelcomeMessage from "@/components/WelcomeMessage.vue";
export default {
  components: {
    WelcomeMessage
  }
};
</script>

<style lang="scss" scoped>
form {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: 70px;

  /* Input ============================== */
  input {
    margin-bottom: 50px;
    padding: 5px 20px;
    border-radius: 50px;
    background-color: transparent;
    border: 3px solid #000;
    outline: none;
    width: 400px;
    height: 50px;
    font: 1.2em sans-serif;

    // Placehoder
    &:focus::placeholder {
      opacity: 0;
      transition: 0.1s;
    }
  }

  /* Button ============================== */
  button {
    font: 2em cursive;
    padding: 10px;
    border-radius: 50px;
    background-color: #0ee0e0;
    border: 2px solid #000;
    padding: 10px 20px;
    outline: none;
    cursor: pointer;

    // Active
    &:active {
      transform: scale(0.8);
      transition: 0.2s;
    }
  }
}
</style>
