<template>
  <main class="login-container">
    <div class="login-image__container">
      <div class="login-logo">
        <img src="/login-logo.png" alt="Logo" />
      </div>
      <div class="login-image">
        <div class="login-image__acheiver">
          <img src="./../assets/images/login-img.png" alt="Logo" />
        </div>
        <div class="login-img__content">
          <h4>Team Achieve</h4>
          <span>Your perfect solution for funding your desires</span>
        </div>
      </div>
    </div>

    <!-- Right - Form -->
    <div class="login-form__container">
      <div class="mobile-logo">
        <img src="/login-logo.png" alt="Logo" />
      </div>

      <div class="login-form__wrapper">
        <div class="login-form__header">
          <h1>Welcome Back</h1>
          <p>Enter your email address and password to access your account.</p>
        </div>

        <form class="login-form">
          <div class="form-group">
            <label for="email" class="form-label">
              Email Address <span class="required">*</span>
            </label>
            <input
              id="email"
              v-model="email"
              type="email"
              class="form-input"
              placeholder="Enter your email"
              required
            />
          </div>

          <div class="form-group">
            <label for="password" class="form-label">
              Password <span class="required">*</span>
            </label>
            <div class="password-input__wrapper">
              <input
                id="password"
                v-model="password"
                :type="showPassword ? 'text' : 'password'"
                class="form-input"
                placeholder="Enter your password"
                required
              />
              <button
                type="button"
                class="password-toggle"
                @click="showPassword = !showPassword"
                aria-label="Toggle password visibility"
              >
                <svg
                  v-if="!showPassword"
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"></path>
                  <circle cx="12" cy="12" r="3"></circle>
                </svg>
                <svg
                  v-else
                  width="20"
                  height="20"
                  viewBox="0 0 24 24"
                  fill="none"
                  stroke="currentColor"
                  stroke-width="2"
                >
                  <path
                    d="M17.94 17.94A10.07 10.07 0 0 1 12 20c-7 0-11-8-11-8a18.45 18.45 0 0 1 5.06-5.94M9.9 4.24A9.12 9.12 0 0 1 12 4c7 0 11 8 11 8a18.5 18.5 0 0 1-2.16 3.19m-6.72-1.07a3 3 0 1 1-4.24-4.24"
                  ></path>
                  <line x1="1" y1="1" x2="23" y2="23"></line>
                </svg>
              </button>
            </div>
          </div>

          <div class="form-options">
            <label class="checkbox-label">
              <input v-model="rememberMe" type="checkbox" class="checkbox" />
              <span>Remember me</span>
            </label>
            <a href="#" class="forgot-password">Forgot Password?</a>
          </div>

          <button type="submit" class="btn btn-primary">Sign in</button>
        </form>

        <div class="signup-link">
          <span>Don't have an account? </span>
          <a href="#">Sign up</a>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped src="../assets/styles/login.css"></style>
