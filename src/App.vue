<template>
  <div id="app">
    <header>
		<div class="header center">
			<div class="header__left">
				<a class="logo" href="index.html">
					<img class="logo__img" src="https://raw.githubusercontent.com/Sergey-TR/testkraken/master/project/img/logo.png" alt="logo">BRAN<span class="logoD">D</span>
				</a>
					<div class="browse">
					<details class="browse_det">
						<summary class="browse_det_sum">Browse</summary>
						<div class="browse_drop_menu">
						<h3 class="browse__h3">Women</h3>
						<ul class="browse_ul">
							<li><a href="women.html" class="browse_a">Dresses</a></li>
							<li><a href="women.html" class="browse_a">Tops</a></li>
							<li><a href="women.html" class="browse_a">Sweaters/Knits</a></li>
							<li><a href="women.html" class="browse_a">Jackets/Coats</a></li>
							<li><a href="women.html" class="browse_a">Blazers</a></li>
							<li><a href="women.html" class="browse_a">Denim</a></li>
							<li><a href="women.html" class="browse_a">Leggings/Pants</a></li>
							<li><a href="women.html" class="browse_a">Skirts/Shorts</a></li>
							<li><a href="women.html" class="browse_a">Accessories</a></li>
						</ul>
						<h3 class="browse__h3">men</h3>
						<ul class="browse_ul">
							<li><a href="men.html" class="browse_a">Tees/Tank tops</a></li>
							<li><a href="men.html" class="browse_a">Shirts/Polos</a></li>
							<li><a href="men.html" class="browse_a">Sweaters</a></li>
							<li><a href="men.html" class="browse_a">Sweatshirts/Hoodies</a></li>
							<li><a href="men.html" class="browse_a">Blazers</a></li>
							<li><a href="men.html" class="browse_a">Jackets/vests</a></li>
						</ul>
						</div>
					</details>
				</div>
					<form class="header__form" action="#">
					<input class="header__form__int" type="search" placeholder="Search for Item...">
					<button class="header__form__btn" type="submit"><i class="fas fa-search"></i></button>
				</form>
			</div>
			<div class="header__right">
			<div class="header__right_cart">
				<div class="cart__total">
					<span class="cart__total_span">0</span>
					<button class="cart__total_btn"></button>
				</div>
				
			</div>
				<!--<a href="cart.html"><img class="header__cart" src="img/cart.png" alt="cart"></a>-->
				<div class="my_account_btn">
					<details class="my_account_det">
						<summary class="my_account_sum">My Account</summary>
						<div class="my_account_checkout">
							<!-- <div class="basket-item"> -->
								<basket ref="basket" />
							<!-- </div> -->
							
								<div class="my_account_total">
									<div class="total">TOTAL</div>
									<div class="total500"><span class="span_total">0</span></div>
								</div>
								<button class="my_account_check">Checkout</button>
								<button class="my_account_cart">Go to cart</button> 

						</div>
					</details>
				</div>
				<!--<a href="#" class="button">My Account</a>-->
			</div>
		</div>
	</header>
    <v-main-wrapper />
  </div>
</template>

<script>
import vMainWrapper from './components/v-main-wrapper'

export default {
  name: 'App',
  components: {
    vMainWrapper
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
header {
  position: fixed;
  top: 0px !important;
  width: 100%;
  z-index: 9999;
}

nav {
  position: fixed;
  top: 102px !important;
  width: 100%;
  z-index: 9998;
  background-color: #ffffff;
}

.empty {
  height: 168px;
}

.header {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  height: 100px;
  background-color: #ffffff;
  border: 1px solid #ececec;
  -webkit-box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.17);
          box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.17);
}

.header__left,
.header__right {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
}

.header__form {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  /*margin-left: 37px;*/
}

.header__form__int {
  height: 38px;
  width: 277px;
  background-color: #ffffff;
  border: 1px solid #e6e6e6;
  font-size: 14px;
  font-weight: 300;
  color: #a4a4a4;
  padding-left: 16px;
  letter-spacing: 0.03em;
  line-height: 32px;
}

.header__form__btn {
  height: 38px;
  width: 38px;
  background-color: #ffffff;
  border: 1px solid #e6e6e6;
}

.browse {
  position: relative;
  width: 87px;
  height: 38px;
  margin-left: 37px;
}

.browse_det {
  position: absolute;
  width: 87px;
  height: 38px;
}

.browse_det_sum {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-pack: distribute;
      justify-content: space-around;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  font-size: 14px;
  font-weight: 300;
  color: #222222;
  letter-spacing: 0.03em;
  line-height: 32px;
  height: 38px;
  width: 87px;
  /*border: 1px solid #e6e6e6;*/
  text-align: center;
  background-color: #e8e8e8;
  outline: none;
}

summary::-webkit-details-marker {
  display: none;
}

/*summary::after {
  content: ' \25BC';
  color: #838383;
  '\25B6';
	padding-right: 0.5em;
}*/

.browse_drop_menu {
  width: 262px;
  height: 481px;
  background-color: white;
  /* opacity: 62%; */
  position: relative;
  z-index: 1;
  padding: 19px 0px 19px 15px;
}

.browse_ul {
  list-style-type: none;
}

.browse__h3 {
  font-size: 14px;
  color: #232323;
  border-bottom: 1px solid #e8e8e8;
  /*text-align: right;*/
  letter-spacing: 0.03em;
  line-height: 32px;
  text-transform: uppercase;
}

.browse_a {
  font-size: 14px;
  color: #4f4f4f;
  text-align: right;
  letter-spacing: 0.03em;
  line-height: 28px;
}

/*details[open] > summary::after {
  content: ' \25BC';
  color: #838383;
}*/

/*.browse_det[open] {
  background-color: #fff;
}*/

.browse_det[open] > .browse_det_sum::after {
  content: ' \25B2';
  color: #838383;
}

.browse_det_sum::after {
  content: ' \25BC';
  color: #838383;
}

.browse_det[open] > .browse_drop_menu {
  width: 262px;
  /*height: 481px;*/
  background-color: #ffffff;
  /* opacity: 62%; */
  position: relative;
  z-index: 1;
  padding: 19px 0px 19px 15px;
}

.header__cart {
  margin-right: 26px;
}

.cart__total {
  background-image: url(https://raw.githubusercontent.com/Sergey-TR/testkraken/master/project/img/cart.png);
  height: 38px;
  width: 40px;
  background-repeat: no-repeat;
  position: relative;
  margin-right: 20px;
  background-position: center;
}

.cart__total_span {
  position: absolute;
  right: -10px;
  top: 0px;
  width: 20px;
  height: 20px;
  border-radius: 50%;
  background-color: #f16d7f;
  color: white;
  text-align: center;
  line-height: 21px;
  font-weight: bold;
}

.cart__total_btn {
  position: absolute;
  width: 40px;
  height: 38px;
  top: 0;
  left: 0;
  border: none;
  outline: none;
  opacity: 0;
  cursor: pointer;
}

.logo {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
  font-size: 27px;
  font-weight: 300;
  color: #3e3e40;
  text-align: center;
  letter-spacing: 0.03em;
  line-height: 32px;
  text-transform: uppercase;
}

.logoD {
  font-size: 27px;
  font-weight: 900;
  color: #f16d7f;
  text-align: center;
  letter-spacing: 0.03em;
  line-height: 32px;
}

.logo__img {
  margin-right: 13px;
}

.my_account_btn {
  position: relative;
  width: 130px;
  height: 38px;
}

.my_account_det {
  position: absolute;
  width: 130px;
  height: 38px;
}

.my_account_det[open] > .my_account_checkout {
  opacity: 0;
  -webkit-transition: all 5s;
  transition: all 5s;
  opacity: 1;
}

.my_account_sum {
  background-color: #f16d7f;
  height: 38px;
  width: 130px;
  font-size: 15px;
  color: #ffffff;
  text-align: right;
  letter-spacing: 0.03em;
  line-height: 32px;
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -ms-flex-pack: distribute;
      justify-content: space-around;
  -webkit-box-align: center;
      -ms-flex-align: center;
          align-items: center;
          outline: none;
}

.my_account_sum::after {
  content: '\25BC';
  color: #ffffff;
}

/*.my_account_checkout {
  height: 440px;
  width: 262px;
  background-color: #ffffff;
  border-radius: 5px;
  top: 54px;
  position: absolute;
  left: -56px;
  right: 0;
  z-index: 1;
}*/

.my_account_checkout {
  /*height: 440px;*/
  width: 262px;
  background-color: #ffffff;
  border-radius: 5px;
  top: 54px;
  position: absolute;
  /* left: -56px; */
  right: 0;
  z-index: 1;
  max-height: 300px;
  /* overflow: scroll; */
  overflow-y: auto;
}

.my_account_top,
.my_account_down {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  width: 230px;
  height: 120px;
  margin-left: 17px;
}

/*.my_account_top_a {
  display: block;
  width: 230px;
  height: 120px;
  position: absolute;
  z-index: 1;
}*/

.my_account_h3 {
  font-size: 12px;
  font-weight: bold;
  color: #222222;
  text-align: right;
  text-transform: uppercase;
  padding: 10px 14px;
}

.my_account_p {
  font-size: 12px;
  color: #f16d7f;
  text-transform: uppercase;
  word-spacing: 3px;
  padding: 2px 15px;
}

.my_account_rezon-img {
  padding-left: 15px;
}

.size_x {
  font-size: 10px;
  color: #f16d7f;
  text-transform: uppercase;
}

/*.account_clear {
  width: 15px;
  height: 15px;
  border-radius: 50%;
  background-image: url(img/krest.png);
  border: none;
  position: absolute;
  top: 40px;
  left: 30px;
}*/

.my_account_img,
.my_account_rezon,
.my_account_clear {
  margin-top: 21px;
  position: relative;
}

.my_account_total {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  -webkit-box-pack: justify;
      -ms-flex-pack: justify;
          justify-content: space-between;
  width: 218px;
  margin: 19px 16px 32px 17px;
}

.total,
.total500 {
  font-size: 16px;
  font-weight: bold;
  color: #222222;
  text-transform: uppercase;
}

.my_account_check,
.my_account_cart {
  width: 225px;
  height: 50px;
  margin-left: 15px;
  margin-bottom: 11px;
}

.my_account_check {
  background-color: #ffffff;
  border: 1px solid #f16d7f;
  font-size: 14px;
  font-weight: bold;
  color: #f16d7f;
  text-transform: uppercase;
}

.my_account_cart {
  background-color: #ffffff;
  border: 1px solid #eaeaea;
  font-size: 14px;
  font-weight: bold;
  color: #4a4a4a;
  text-transform: uppercase;
}
</style>
