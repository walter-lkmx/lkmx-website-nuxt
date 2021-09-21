<template>
  <div class="home__vision">
    <p>// homepage</p>
    <h3>tecnología, creatividad, innovación</h3>
  </div>
</template>

<script>
export default {
  methods: {
    change(){
      var h =document.querySelector('h1');
      var p= h.getBoundingClientRect();
      var c= document.querySelector('.cursor');

      document.body.onmousemove = function(e) {
        /*Adjust the cursor position*/
        c.style.left=e.clientX+'px';
        c.style.top=e.clientY+'px';
        /*Adjust the clip-path*/
        h.style.setProperty('--x',(e.clientX-p.top)+'px');
        h.style.setProperty('--y',(e.clientY-p.left)+'px');
      }
    }
  },
  mounted(){
    // this.change();
  }
}
</script>

<style lang="scss">
// body {
//   // cursor:none;
// }
// h1 {
//   color: #000;
//   display:inline-block;
//   margin:50px;
//   text-align: center;
//   position:relative;
// }
// h1:before {
//   position:absolute;
//   content:attr(data-text);
//   color:#fff;
//   // background:#000;
//   clip-path: circle(20px at var(--x,-100%) var(--y,-100%));
// }
// .cursor {
//   position:fixed;
//   width:40px;
//   height:40px;
//   // background:#000;
//   border-radius:50%;
//   top:0;
//   left:0;
//   // transform:translate(-50%,-50%);
//   // z-index:-2;
// }
.home__vision {
  transform: rotate(-90deg);
  position: fixed;
  z-index: 10;
  left: -154px;
  top: 300px;
  * {
    margin: 0;
  }
  p {
    font-family: var(--f-mono-text-font);
    color: var(--color-accent-pink);
  }
  h3 {
    font-size: 24px;
    // color: var(--color-neutral-white);
    // filter: hue-rotate(90deg);
    color: white;
    // mix-blend-mode: difference;
    // filter: invert(1);
// mix-blend-mode: difference;
  //   filter: invert(100%);
	// -moz-background-clip: text;
	// -webkit-background-clip: text;
  }
}
</style>