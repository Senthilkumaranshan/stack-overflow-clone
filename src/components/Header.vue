<template>
    <div class="p-header__inner">
        <h1 class="p-header__logo">All Questions</h1>
        <nav class="p-header__nav p-header-nav" aria-label="firstnav">
            <ul class="p-header-nav__items">
                <li class="p-header-nav__item p-header-nav__item--contact"><a href="">Ask Question</a></li>
            </ul>
        </nav>
    </div>
        <div class="p-header__inner">
        <p class="" id="questions">18, 774, 971 questions</p>
        <nav class="p-header__nav p-header-nav" id="secondnav" aria-label="secondnav">
        <div class="tabs">
  <div class="tab-button-outer">
    <ul id="tab-button">
      <li><a href="#tab01">Newest</a></li>
      <li><a href="#tab02">Active</a></li>
      <li><a href="#tab03">Bountied</a></li>
      <li><a href="#tab04">Unanswered</a></li>
      <li><a href="#tab05">More</a></li>
    </ul>
  </div>
  <div class="tab-select-outer">
    <select id="tab-select">
      <option value="#tab01">Newest</option>
      <option value="#tab02">Active</option>
      <option value="#tab03">Bountied</option>
      <option value="#tab04">Unanswered</option>
      <option value="#tab05">More</option>
    </select>
  </div>
</div>

            <ul class="p-header-nav__items filterul">
                <li class="p-header-nav__item p-header-nav__item--contact" id="filter"><a href="">Filter</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>

main {
	width: 100%;
}
a {
	text-decoration: none;
}

section:first-of-type {
  position: relative;
  height: 100vh;
  background-color: blue;
}
section:nth-of-type(2) {
  height: 100vh;
  background-color: yellow;
}
section:nth-of-type(3) {
  height: 100vh;
  background-color: red;
}
section:nth-of-type(2) {
  height: 100vh;
  background-color: blue;
}
.p-header {
  position: sticky;
  top: 0;
  left: 0;
  width: 100%;

  background-color: pink;
  height: 100px;
  z-index: 100;
}
.p-header__inner {
  display: flex;
 /* align-items: center;*/
  height: inherit;
	  padding: 0 40px;
}
.p-header__logo {
  font-size: 32px;
  line-height: 1;
  font-weight: 500;
  width: 200px;
  color: #000000;
}
.p-header__nav {
  margin-left: auto;
  height: inherit;
}


  
.p-header-nav {
  font-size: rem(16);
  font-weight: 500;
  line-height: calc(24 / 16);
  letter-spacing: 0.1em;
  color: black;
}
.p-header-nav__items {
  display: flex;
  align-items: center;
  height: inherit;
}
.p-header-nav__item {
  position: relative;
  height: inherit;
  display: flex;
  align-items: center;
}
.p-header-nav__item:not(:first-of-type) {
  margin-left: 10px;
}
.p-header-nav__item a {
	color: yellow;
  display: inline-block;
  padding: 12px 10px;
  transition: opacity .3s;
}

.p-header-nav__item span {
  position: relative;
}
.p-header-nav__item span::after {
  position: absolute;
  bottom: -4px;
  left: 0;
  content: '';
  display: inline-block;
  width: 100%;
  height: 1px;
  background-color: brown;
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.2s;
}
.p-header-nav__item:hover span::after,.p-header-nav__item a:focus span::after {
  transform: scaleX(1);
}
.p-header-nav__item--contact a {
  padding: 12px 19px;
  color: #FFF;
  background-color: #00ABF0;
  border-radius: 2px;
}
.p-header-nav__item--contact a:hover {
	opacity: .7;
}

.p-header-nav__drop-down > a {
  pointer-events: none;
}

.p-header-nav__drop-down-items {
  position: absolute;
  top: 100%;
  transform: translateX(-40%) ;
  width: 450px;
  display: flex;
  justify-content: center;
  background-color: blue;
  opacity: 0;
  visibility: hidden;
  transition: opacity .5s, visibility .5s;
}

.p-header-nav__drop-down:hover .p-header-nav__drop-down-items, .p-header-nav__drop-down:focus-within .p-header-nav__drop-down-items{
  opacity: 1;
  visibility: visible;
}

.p-header-nav__drop-down-item img {
  width: 100%;
  height: auto;
  object-fit: cover;
  aspect-ratio: 180 / 130;
}
.p-header-nav__drop-down-item a {
  padding: 15px;
}
.p-header-nav__drop-down-item p {
  margin-top: 10px;
  text-align: center;
}
#filter a {
    background-color: #CDF0FF !important;
    color: #00ABF0;
}

.tabs {
  max-width: 640px;
  margin: 0 auto;
  padding: 0 20px;
}
#tab-button {
  display: table;
  table-layout: fixed;
  width: 100%;
  margin: 0;
  padding: 0;
  list-style: none;
}
#tab-button li {
  display: table-cell;
  width: 20%;
}
#tab-button li a {
  display: block;
  padding: .5em;
  background: #eee;
  border: 1px solid #ddd;
  text-align: center;
  color: #000;
  text-decoration: none;
}
#tab-button li:not(:first-child) a {
  border-left: none;
}
#tab-button li a:hover,
#tab-button .is-active a {
  border-bottom-color: transparent;
  background: #fff;
}
.tab-contents {
  padding: .5em 2em 1em;
  border: 1px solid #ddd;
}



.tab-button-outer {
  display: none;
}
.tab-contents {
  margin-top: 20px;
}

.filterul {
    float: right !important;
    padding: 0px !important;
    margin-top: -45px !important;
}

#secondnav {
    margin-left: 25%;
    width: 100%;
}

#questions {
    width: 300px;
}
@media screen and (min-width: 768px) {
  .tab-button-outer {
    position: relative;
    z-index: 2;
    display: block;
  }
  .tab-select-outer {
    display: none;
  }
  .tab-contents {
    position: relative;
    top: -1px;
    margin-top: 0;
  }
}
</style>