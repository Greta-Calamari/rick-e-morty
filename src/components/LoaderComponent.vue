<template>
<div>
	<div class="mosaic-loader">
    <div class="cell d-0"></div>
    <div class="cell d-1"></div>
    <div class="cell d-2"></div>
    <div class="cell d-3"></div>
    <div class="cell d-1"></div>
    <div class="cell d-2"></div>
    <div class="cell d-3"></div>
    <div class="cell d-4"></div>
    <div class="cell d-2"></div>
    <div class="cell d-3"></div>
    <div class="cell d-4"></div>
    <div class="cell d-5"></div>
    <div class="cell d-3"></div>
    <div class="cell d-4"></div>
    <div class="cell d-5"></div>
    <div class="cell d-6"></div>
</div>

</div>
<!-- <div class="preloader">
	<div class="box">
		<div class="box__inner">
			<div class="box__back-flap"></div>
			<div class="box__right-flap"></div>
			<div class="box__front-flap"></div>
			<div class="box__left-flap"></div>
			<div class="box__front"></div>
		</div>
	</div>
	<div class="box">
		<div class="box__inner">
			<div class="box__back-flap"></div>
			<div class="box__right-flap"></div>
			<div class="box__front-flap"></div>
			<div class="box__left-flap"></div>
			<div class="box__front"></div>
		</div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
	<div class="line">
		<div class="line__inner"></div>
	</div>
</div> -->
  
</template>

<script>
export default {
    name: 'LoaderComponent'
}
</script>

<style lang="scss">
// :root {
// 	--dur: 2s;
// 	--bg: #e3e4e8;
// 	--fg: #17181c;
// 	font-size: calc(12px + (24 - 12)*(100vw - 320px)/(2560 - 320));
// }
// // body {
// // 	background: var(--bg);
// // 	color: var(--fg);
// // 	display: flex;
// // 	font: 1em/1.5 sans-serif;
// // 	height: 100vh;
// // 	overflow: hidden;
// // }
// .preloader, .box, .box__inner, .box__inner div  {
// 	transform-style: preserve-3d;
// }
// .preloader {
// 	margin: auto;
// 	position: relative;
// 	width: 12em;
// 	height: 24em;
// }
// .box, .box__inner, .box__inner div, .line {
// 	position: absolute;
// }
// .box, .box__inner div, .line__inner  {
// 	animation-timing-function: ease-in-out;
// 	animation-iteration-count: infinite;
// }
// .box, .line__inner {
// 	animation-duration: var(--dur);
// }
// .box__inner div, .line__inner {
// 	background: var(--fg);
// }
// /* Boxes */
// .box, .box__inner {
// 	width: 100%;
// 	height: 50%;
// }
// .box {
// 	animation-name: popOut;
// 	top: 50%;
// 	perspective: 25em;
// 	transform-origin: 50% 75%;
// 	z-index: 1;
// }
// .box + .box {
// 	animation-delay: calc(var(--dur)/-2);
// }
// .box__inner, .box__inner div  {
// 	animation-delay: inherit;
// 	animation-duration: inherit;
// }
// .box__inner {
// 	transform: rotateX(50deg);
// 	transform-origin: 50% 25%;
// }
// .box__inner div {
// 	box-shadow: 0 0 0 0.2em var(--bg) inset;
// }
// .box__back-flap, .box__front-flap, .box__front {
// 	width: 6em;
// }
// .box__left-flap, .box__right-flap, .box__front {
// 	height: 6em;
// }
// .box__back-flap, .box__front-flap {
// 	left: 3em;
// 	height: 3em;
// }
// .box__left-flap, .box__right-flap {
// 	top: 3em;
// 	width: 3em;
// }
// .box__back-flap {
// 	animation-name: backFlap;
// 	transform: rotateX(-180deg);
// 	transform-origin: 50% 100%;
// }
// .box__right-flap {
// 	animation-name: rightFlap;
// 	left: 9em;
// 	transform: rotateY(-179deg);
// 	transform-origin: 0 50%;
// }
// .box__front-flap {
// 	animation-name: frontFlap;
// 	top: 9em;
// 	transform: rotateX(180deg);
// 	transform-origin: 50% 0;
// }
// .box__left-flap {
// 	animation-name: leftFlap;
// 	transform: rotateY(179deg);
// 	transform-origin: 100% 50%;
// }
// .box__front {
// 	top: 3em;
// 	left: 3em;
// 	transform: rotateX(-90deg) translateY(50%) translateZ(3em);
// }
// /* Lines */
// .line, .line__inner {
// 	border-radius: 0.1em;
// }
// .line {
// 	top: 0;
// 	left: calc(50% - 0.1em);
// 	width: 0.2em;
// 	height: 6em;
// 	overflow: hidden;
// 	transform-origin: 50% 0.1em;
// }
// .line:nth-child(n + 5) {
// 	top: 90%;
// 	transform: translateY(2em);
// }
// .line:nth-child(3) {
// 	left: calc(50% - 1.1em);
// }
// .line:nth-child(4) {
// 	left: calc(50% + 0.9em);
// }
// .line:nth-child(5) {
// 	transform: rotate(-90deg) translateY(2em);
// }
// .line:nth-child(6) {
// 	transform: rotate(-45deg);
// }
// .line:nth-child(7) {
// 	transform: translateY(-0.5em);
// }
// .line:nth-child(8) {
// 	transform: rotate(45deg);
// }
// .line:nth-child(9) {
// 	transform: rotate(90deg) translateY(2em);
// }
// .line__inner {
// 	animation-duration: calc(var(--dur)/2);
// 	width: 100%;
// 	height: 100%;
// }
// .line:nth-child(n + 3):nth-child(-n + 4) .line__inner {
// 	animation-name: falling;
// }
// .line:nth-child(n + 5):nth-child(-n + 9) .line__inner {
// 	animation-name: landing;
// 	transform: translateY(-100%);
// }
// /* Dark Mode */
// @media (prefers-color-scheme: dark) {
// 	:root {
// 		--bg: #17181c;
// 		--fg: #e3e4e8;
// 	}
// }
// /* Animations */
// @keyframes backFlap {
// 	from, 33% { transform: rotateX(-180deg); }
// 	41% { transform: rotateX(10deg); }
// 	45% { transform: rotateX(-27deg); }
// 	50%, to { transform: rotateX(-15deg); }
// }
// @keyframes rightFlap {
// 	from, 33% { transform: rotateY(-179deg); }
// 	41% { transform: rotateY(10deg); }
// 	45% { transform: rotateY(-27deg); }
// 	50%, to { transform: rotateY(-15deg); }
// }
// @keyframes frontFlap {
// 	from, 33% { transform: rotateX(180deg); }
// 	41% { transform: rotateX(-10deg); }
// 	45% { transform: rotateX(27deg); }
// 	50%, to { transform: rotateX(15deg); }
// }
// @keyframes leftFlap {
// 	from, 33% { transform: rotateY(179deg); }
// 	41% { transform: rotateY(-10deg); }
// 	45% { transform: rotateY(27deg); }
// 	50%, to { transform: rotateY(15deg); }
// }
// @keyframes popOut {
// 	from, 21% { transform: translateZ(1px) translateY(0) scale(0,0); }
// 	33% { transform: translateZ(1px) translateY(-100%) scale(0.75,1.5); }
// 	41% { transform: translateZ(1px) translateY(-100%) scale(1,1); }
// 	42%,50% { transform: translateZ(0) translateY(-100%) scale(1,1); }
// 	55% { transform: translateZ(0) translateY(-100%) scale(0.75,1.5); }
// 	60% { transform: translateZ(0) translateY(0) scale(1.5,0.75); }
// 	67% { transform: translateZ(0) translateY(0) scale(1,1); }
// 	to { transform: translateZ(0) translateY(0) scale(0,0); }
// }
// @keyframes falling {
// 	from, 12% { transform: translateY(0%); }
// 	28%, to { transform: translateY(100%); }
// }
// @keyframes landing {
// 	from, 17% { transform: translateY(-100%); }
// 	41%, to { transform: translateY(100%); }
// }

$--p-1: #d4aee0;
$--p-2: #8975b4;
$--p-3: #64518a;
$--p-4: #565190;

$--b-1: #44abac;
$--b-2: #2ca7d8;
$--b-3: #1482ce;
$--b-4: #05597c;

$--g-1: #b2dd57;
$--g-2: #57c443;
$--g-3: #05b853;
$--g-4: #19962e;

$--y-1: #fdc82e;
$--y-2: #fd9c2e;
$--y-3: #d5385a;
$--y-4: #911750;

$--s-1: #d9d9d9;
$--s-2: #9e9e9e;
$--s-3: #666666;
$--s-4: #2b2b2b;

$colors: (
  $--p-1,
  $--p-2,
  $--p-3,
  $--p-4,
  $--b-1,
  $--b-2,
  $--b-3,
  $--b-4,
  $--g-1,
  $--g-2,
  $--g-3,
  $--g-4,
  $--y-1,
  $--y-2,
  $--y-3,
  $--y-4,
);

h2 {
  display: block;
  color: white;
  font-weight: 100;
  //margin-right: 2rem;
  text-align: center;
}

@import url('https://fonts.googleapis.com/css2?family=Lato:wght@100;300;400&display=swap');

body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
//   min-height: 100vh;
//   margin: 0;
//   font-family: 'Lato';
//   font-weight: 300;
//   font-size: 24px;
//   background: $--s-4;
}

.mosaic-loader {
  --cell-size: 64px;
  --cell-spacing: 1px;
  --border-width: 1px;
  --cells: 4;
  --total-size: calc(var(--cells) * (var(--cell-size) + 2 * var(--cell-spacing)));
  
  display: flex;
  flex-wrap: wrap;
  width: var(--total-size);
  height: var(--total-size);
  
  > .cell {
    --cell-color: white;
    flex: 0 0 var(--cell-size);
    margin: var(--cell-spacing);
    background-color: transparent;
    box-sizing: border-box;
    border: var(--border-width) solid var(--cell-color);
    
    animation: 1.5s ripple ease infinite;
    
    $delays: (2 * 4) - 2;
    @for $i from 1 through $delays {
      &.d-#{$i} {
        animation-delay: $i * 100ms;
      }
    }
    
    @for $i from 1 through length($colors) {
      &:nth-child(#{$i}) {
        --cell-color: #{nth($colors, $i)};
      }
    }
  }
}

@keyframes ripple {
  0% {
    background-color: transparent;
  }
  
  30% {
    background-color: var(--cell-color);
  }
  
  60% {
    background-color: transparent;
  }
  
  100% {
    background-color: transparent;
  }
}
</style>