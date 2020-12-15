<template>
  <div class="flex-center">
    <div class="login-card">
      <form class="login-form">
        <h1>Create a new account</h1>
        <div class="form-group">
          <label for="email">Your E-mail</label>
          <input type="email" id="email">
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input type="password" id="password">
        </div>
        <div class="terms">
          <a href="#terms">
            <small>Terms and conditions</small>
          </a>
        </div>
        <button type="submit">Sign up</button>
      </form>
    </div>
  </div>
</template>

<style lang="scss" scoped>
  .login {
    &-card {
      width: 300px;
      background: white;
      box-shadow: 0 18px 30px rgba(0,0,0,0.06);
      padding: 3rem;
      border-radius: 8px;
      text-align: left;
      h1 {
        margin-top: 0;
        margin-bottom: 1em;
        font-size: 3em;
        letter-spacing: -2px;
      }
      button {
        padding: 20px;
        background-color: #42b983;
        border: none;
        border-radius: 4px;
        display: block;
        width: 100%;
        color: white;
        font-weight: 600;
        cursor: pointer;
        &:hover {
          background-color: #42b96a;
        }
      }
    }
  }
  .form-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 2rem;
    input {
      border: none;
      border-bottom: 1px solid #afafaf;
      padding: 10px 5px;
    }
    label {
      margin-bottom: 5px;
      color: #afafaf;
      font-size: 0.7rem;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    &:hover {
      input {
        border-bottom-color: #8d8d8d;
      }
      label {
        color: #8d8d8d;
      }
    }
  }

  .form-group input:focus {
    outline: none;
    border-bottom-color: #42b983;
    background-color: #f7f7f7;
  }
  .terms {
    a {
      color: darkgray;
      text-decoration: none;
      &:hover {
        color: gray;
      
      }
    }
    text-align: center;
    margin-bottom: 1rem;
  }
</style>