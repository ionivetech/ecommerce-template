<template>
  <footer>
    <div class="container">
      <!-- Subscribe -->
      <div class="subscribe">
        <h2>Register now so you don't miss our programs</h2>

        <div class="subscribe__form">
          <input
            type="email"
            placeholder="Enter your Email"
            class="subscribe__form__input"
          />
          <button class="subscribe__form__button">Subscribe Now</button>
        </div>
      </div>

      <!-- Menu & Social media -->
      <div class="link">
        <div class="link__menu">
          <a
            href="#"
            class="link__menu__list"
          >
            Home
          </a>
          <a
            href="#"
            class="link__menu__list"
          >
            Category
          </a>
          <a
            href="#"
            class="link__menu__list"
          >
            About
          </a>
          <a
            href="#"
            class="link__menu__list"
          >
            Contact
          </a>
        </div>

        <div class="link__social-media">
          <a href="#">
            <img
              src="@/assets/icons/facebook.svg"
              width="20"
              height="20"
              alt="facebook-icons"
            />
          </a>
          <a href="#">
            <img
              src="@/assets/icons/twitter.svg"
              width="20"
              height="20"
              alt="twitter-icons"
            />
          </a>
          <a href="#">
            <img
              src="@/assets/icons/instagram.svg"
              width="20"
              height="20"
              alt="instagram-icons"
            />
          </a>
          <a href="#">
            <img
              src="@/assets/icons/youtube.svg"
              width="20"
              height="20"
              alt="youtube-icons"
            />
          </a>
        </div>
      </div>

      <!-- Copyright & policy -->
      <div class="copyright-policy">
        <p class="copyright-policy__copyright">© 2022 Monito. All rights reserved.</p>
        <img
          src="@/assets/logo.svg"
          width="115"
          height="40"
          alt="footer-logo"
        />
        <div class="copyright-policy__link">
          <a
            href="#"
            class="copyright-policy__link__list"
          >
            Terms of Service
          </a>
          <a
            href="#"
            class="copyright-policy__link__list"
          >
            Privacy Policy
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
footer {
  padding: 40px 0px 20px 0px;
  margin-top: 40px;
  background: linear-gradient(102.87deg, #fceed5 6.43%, #fceed5 78.33%, #ffe7ba 104.24%);
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;

  .subscribe {
    display: flex;
    flex-direction: column;
    gap: 16px;
    background-color: $primary;
    padding: 1rem;
    border-radius: 16px;

    h2 {
      font-size: 20px;
      font-weight: 700;
      line-height: 32px;
      text-align: left;
      color: white;
    }

    &__form {
      display: flex;
      flex-direction: column;
      padding: 12px;
      border-radius: 8px;
      background-color: white;
      gap: 12px;

      &__input {
        box-sizing: border-box;
        height: 48px;
        padding: 0px 28px;
        border: 1px solid $gray;
        border-radius: 8px;

        &:focus {
          outline: none;
          border-color: $primary;
        }
      }

      &__button {
        width: 100%;
        height: 48px;
        background-color: $primary;
        color: white;
        font-size: 16px;
        font-weight: 500;
        line-height: 24px;
        border-radius: 8px;
        border: none;
      }
    }

    @media screen and (min-width: $medium) {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
      padding: 2rem;

      h2 {
        width: 389px;
      }
      &__form {
        width: 100%;
        flex-direction: row;
        align-items: center;

        &__input {
          width: 100%;
        }
        &__button {
          max-width: 163px;
        }
      }
    }
  }

  .link {
    margin: 40px 0;
    padding-bottom: 40px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 20px;
    border-bottom: 1px solid #ccd1d2;

    &__menu {
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 8px;

      &__list {
        font-size: 16px;
        font-weight: 500;
        line-height: 24px;
        color: $neutral;
      }
    }

    &__social-media {
      display: flex;
      align-items: center;
      gap: 40px;
    }

    @media screen and (min-width: $medium) {
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      gap: 20px;

      &__menu {
        width: max-content;
        justify-content: flex-start;
        gap: 60px;
      }
    }
  }

  .copyright-policy {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas:
      'logo'
      'link'
      'copyright';

    &__copyright {
      grid-area: copyright;
      justify-self: center;
      font-size: 10px;
      font-weight: 400;
      line-height: 16px;
      color: $neutral-light;
    }

    img {
      grid-area: logo;
      justify-self: center;
      margin-bottom: 32px;
    }

    &__link {
      grid-area: link;
      justify-self: center;
      display: flex;
      gap: 12px;
      margin-bottom: 8px;

      &__list {
        font-size: 12px;
        font-weight: 500;
        line-height: 18px;
        color: $neutral-light;
      }
    }

    @media screen and (min-width: $medium) {
      grid-template-columns: repeat(3, 1fr);
      grid-template-areas: 'copyright logo link';

      &__copyright {
        justify-self: start;
        align-self: center;
        font-size: 14px;
        line-height: 20px;
      }
      img {
        margin-bottom: 0;
        align-self: center;
      }
      &__link {
        justify-self: end;
        align-self: center;

        &__list {
          font-size: 14px;
          line-height: 20px;
        }
      }
    }
  }

  @media screen and (min-width: $medium) {
    border-top-left-radius: 40px;
    border-top-right-radius: 40px;
  }
}
</style>
