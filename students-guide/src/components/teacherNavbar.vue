<template>
  <!-- <div>
  <nav class="page__menu page__custom-settings menu">
    <ul class="menu__list r-list">
      <li class="menu__group">
        <router-link to="/homeT"
          ><a class="menu__link r-link text-underlined" >home</a></router-link
        >
      </li>
      <li class="menu__group">
        <router-link to="/post"><a
          
          class="menu__link r-link text-underlined"
          >Post</a
        ></router-link>
      </li>
      <li class="menu__group">
       <router-link to="/profil"> <a
          
          class="menu__link r-link text-underlined"
          >Profil</a
        ></router-link>
      </li>
      <li id="logout" class="menu__group">
        <router-link to="/signin">
        <a
          class="menu__link r-link text-underlined"
          v-on:click="logout"
          >logout</a
        >
        </router-link>
      </li>
    </ul>
  </nav>
  </div> -->
  <div>
    <div class="page">
      <nav class="page__menu page__custom-settings menu">
        <ul class="menu__list r-list" id="hasaka">
          <li class="menu__group">
            <router-link to="/homeT"
              ><a href="#0" class="menu__link r-link text-underlined"
                >Home</a
              ></router-link
            >
          </li>
          <li class="menu__group">
            <router-link to="/post"
              ><a href="#0" class="menu__link r-link text-underlined"
                >Post</a
              ></router-link
            >
          </li>
          <li class="menu__group">
            <router-link to="/profil"
              ><a href="#0" class="menu__link r-link text-underlined"
                >Profile</a
              ></router-link
            >
          </li>
          <li class="menu__group">
            <a id="logout" href="#0" class="menu__link r-link text-underlined"
              >logout</a
            >
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  methods:{
   logout(){
    localStorage.clear();
  } 
  }
};
</script>

<style scoped>
/*
=====
DEPENDENCES
=====
*/

.r-link {
  display: var(--rLinkDisplay, inline-flex) !important;
}

.r-link[href] {
  color: var(--rLinkColor) !important;
  text-decoration: var(--rLinkTextDecoration, none) !important;
}

.r-list {
  padding-left: var(--rListPaddingLeft, 0) !important;
  margin-top: var(--rListMarginTop, 0) !important;
  margin-bottom: var(--rListMarginBottom, 0) !important;
  list-style: var(--rListListStyle, none) !important;
}

/*
=====
CORE STYLES
=====
*/

.menu {
  --rLinkColor: var(--menuLinkColor, currentColor);
}

.menu__link {
  display: var(--menuLinkDisplay, block);
}

/* 
focus state 
*/

.menu__link:focus {
  outline: var(--menuLinkOutlineWidth, 2px) solid
    var(--menuLinkOutlineColor, currentColor);
  outline-offset: var(--menuLinkOutlineOffset);
}

/* 
fading siblings
*/

.menu:hover .menu__link:not(:hover) {
  --rLinkColor: var(--menuLinkColorUnactive, rgba(255, 255, 255, 0.35));
}

/*
=====
PRESENTATION STYLES
=====
*/

.menu {
  background-color: var(--menuBackgroundColor, #f0f0f0);
  box-shadow: var(
    --menuBoxShadow,
    0 1px 3px 0 rgba(0, 0, 0, 0.12),
    0 1px 2px 0 rgba(0, 0, 0, 0.24)
  );
}

.menu__list {
  display: flex;
}

.menu__link {
  padding: var(--menuLinkPadding, 1.5rem 2.5rem);
  font-weight: 700;
  text-transform: uppercase;
}
#logout {
  margin-left: 450%;
}

/* 
=====
TEXT UNDERLINED
=====
*/

.text-underlined {
  position: relative;
  overflow: hidden;

  will-change: color;
  transition: color 0.25s ease-out;
}

.text-underlined::before,
.text-underlined::after {
  content: "";
  width: 0;
  height: 3px;
  background-color: var(--textUnderlinedLineColor, currentColor);

  will-change: width;
  transition: width 0.1s ease-out;

  position: absolute;
  bottom: 0;
}

.text-underlined::before {
  left: 50%;
  transform: translateX(-50%);
}

.text-underlined::after {
  right: 50%;
  transform: translateX(50%);
}

.text-underlined:hover::before,
.text-underlined:hover::after {
  width: 100%;
  transition-duration: 0.2s;
}

/*
=====
SETTINGS
=====
*/

.page__custom-settings {
  --menuBackgroundColor: rgb(77, 112, 209);
  --menuLinkColor: #ffffff;
  --menuLinkColorUnactive: #aacfff;
  --menuLinkOutlineOffset: -0.5rem;
  margin-top: 15px;
  border-radius: 12px;
  width: 1200px;
  margin-left: -290px;
}

/*
=====
DEMO
=====
*/

body {
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Open Sans,
    Ubuntu, Fira Sans, Helvetica Neue, sans-serif;
  margin: 0;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

.page {
  box-sizing: border-box;
  max-width: 640px;
  padding-left: 0.75rem;
  padding-right: 0.75rem;
  margin: auto;
}

.page__menu:nth-child(n + 2) {
  margin-top: 3rem;
}

.substack {
  border: 1px solid #eee;
  background-color: #fff;
  width: 100%;
  max-width: 480px;
  height: 280px;
  margin: 1rem auto;
}

.linktr {
  display: flex;
  justify-content: center;
  background-color: rgb(209, 246, 255);
  padding: 2rem;
  text-align: center;
}

.linktr__goal {
  border: 2px solid rgb(255, 255, 255);
  background-color: rgb(255, 255, 255);
  color: rgb(8, 49, 112);
  box-shadow: rgb(8 49 112 / 24%) 0px 2px 8px 0px;
  border-radius: 2rem;
  padding: 0.5rem 1.25rem;
}

.r-link {
  --uirLinkDisplay: var(--rLinkDisplay, inline-flex);
  --uirLinkTextColor: var(--rLinkTextColor);
  --uirLinkTextDecoration: var(--rLinkTextDecoration, none);

  display: var(--uirLinkDisplay) !important;
  color: var(--uirLinkTextColor) !important;
  text-decoration: var(--uirLinkTextDecoration) !important;
}
</style>
