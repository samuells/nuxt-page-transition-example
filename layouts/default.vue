<template>
  <div>
    <nuxt/>
  </div>
</template>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  overflow-x: hidden;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}

.page {
  position: absolute;
  left: 0;
  top: 0;
  right: 0;
  min-height: 100vh;
  background-color: #fff;
}

.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}

.links {
  padding-top: 15px;
}

.wrapper {
  margin: 100px auto;
  width: 500px;
  text-align: center;
}

.wrapper h1 {
  font-size: 60px;
  font-weight: normal;
}

.page-enter-active,
.page-leave-active,
.page-enter-active::before,
.page-enter-active::after,
.page-leave-active::before,
.page-leave-active::after {
  transition: transform 650ms cubic-bezier(.17,.67,.54,.98);
}

.page-enter-active::before,
.page-leave-active::before {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  width: 100%;
  background: url(~assets/bg-transition_parts.png) repeat-y left center;
  z-index: 1000;
}

.page-enter-active::before {
  left: -417px;
}

.page-leave-active::before {
  right: -417px;
}

.page-enter-active::after,
.page-leave-active::after {
  content: '';
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  background-color: #fff;
}

.page-leave::before {
  transform: translate3d(calc(-100% - 417px), 0, 0) scaleX(-1);
}

.page-leave-to::before {
  transform: scaleX(-1);
}

.page-leave::after {
  transform: translate3d(calc(-100% - 417px), 0, 0);
}

.page-enter-to::before,
.page-enter-to::after {
  transform: translate3d(calc(100% + 417px), 0, 0);
}
</style>
