<template>
  <div class="flex-center">
    <div class="login-card">
      <form class="login-form">
        <h1>Create a new account</h1>
        <div class="form-group">
          <label for="name">Your name</label>
          <input type="name" id="name">
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password">
        </div>
        <button type="submit">Sign up</button>
      </form>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .login {
    &-card {
      width: 360px;
      background: white;
      box-shadow: 0 0 30px rgba(0,0,0,0.1);
      padding: 3rem;
      h1 {
        margin-top: 0;
      }
    }
  }
  .form-group {
    display: flex;
    flex-direction: column;
  }

</style>