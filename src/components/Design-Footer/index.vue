<template>
  <footer class="footer">
    <div class="container">
      <div class="row">
        <div class="col-6 d-flex">
          <div class="footer__logo">
            <a href="/"><Logo /></a>
          </div>
          <div class="footer__menu menu">
            <h5 class="menu__title">Office Design Services</h5>
            <ul class="list">
              <li class="list__item">
                <a class="list__link" href="#">How it work</a>
              </li>
              <li class="list__item">
                <a class="list__link" href="#">About us</a>
              </li>
              <li class="list__item">
                <a class="list__link" href="#">Blog</a>
              </li>
              <li class="list__item">
                <a class="list__link" href="#">Login</a>
              </li>
            </ul>
          </div>
        </div>
        <div class="col-6">
          <div>
            <h5 class="menu__title">Sign Up To Our Newsletter</h5>
            <div class="subscribe">
              <input
                placeholder="Email"
                class="subscribe__input"
                type="text"
                name="Email"
              />
              <button class="subscribe__button">Subscribe</button>
            </div>
            <div class="contact">
              <h6>Contact</h6>
              <p>hello@halallab.co</p>
              <p>Skype: masum.parvez/n</p>
              <p>WhatsApp: +8801616-377573</p>
            </div>
          </div>
          <div class="social">
            <a href="#" class="social__link"
              ><i class="fab fa-facebook-f"></i
            ></a>
            <a href="#" class="social__link"><i class="fab fa-dribbble"></i></a>
            <a href="#" class="social__link"><i class="fab fa-behance"></i></a>
            <a href="#" class="social__link"
              ><i class="fab fa-linkedin-in"></i
            ></a>
            <a href="#" class="social__link"><i class="fab fa-skype"></i></a>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Logo from "../logo"
export default {
  name: "Design-Footer",
  components: {
    Logo,
  },
}
</script>

<style scoped lang="scss">
@import "../../assets/scss/variables.scss";
a {
  text-decoration: none;
  color: inherit;
}
.footer {
  position: relative;
  &::before {
    content: "";
    position: absolute;
    width: 234px;
    height: 234px;
    background-image: url("/img/footer-circule.svg");
    bottom: 0;
    left: 0;
  }
  padding: 7.5rem 0;
  &__logo {
    flex: 2;
  }
  &__menu {
    flex: 3;
  }
}
.list {
  display: flex;
  flex-direction: column;
  margin: 1rem 0;
  padding: 0;
  list-style: none;
  &__item {
    margin: 0.5rem 0;
  }
  &__link {
    text-decoration: none;
    color: $secondary-text;
  }
}
.menu {
  &__title {
    font-size: 1.5rem;
    font-weight: 700;
  }
}
.subscribe {
  margin: 1.5rem 2rem 0 0;
  display: flex;
  &__input {
    width: 100%;
    border: none;
    background-color: #f1f4f5;
    margin-right: 1.8rem;
    padding-left: 2.5rem;
    border-bottom-left-radius: 100px;
    border-top-left-radius: 100px;
    outline: none;
  }
  &__button {
    border: none;
    background-color: $primary-color;
    color: $white;
    width: 250px;
    height: 70px;
    font-weight: bold;
    border-top-right-radius: 100px;
    border-bottom-right-radius: 100px;
  }
}
.contact {
  margin-top: 2.7rem;
  h6 {
    font-size: 1.5rem;
    font-weight: 700;
    margin-bottom: 1.5rem;
  }
}
.social {
  display: flex;
  margin-top: 2.5rem;
  &__link {
    font-size: 1.4rem;
    margin-right: 1.5rem;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #f4f4f5;
    border-radius: 50%;
    text-decoration: none;
    color: $main-text;
    width: 60px;
    height: 60px;
  }
}
</style>
