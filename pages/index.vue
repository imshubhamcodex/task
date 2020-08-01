<template>
  <div class="container">
      <h1 class="title">
        Go to form
      </h1>
      <nuxt-link to='/form'><button class="btn-round" >&#8594;</button></nuxt-link>
  </div>
</template>

<script>
export default {}
</script>

<style>
html{
	 overflow-y:hidden;
}
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  color: #35495e;
  letter-spacing: 1px;
}
.btn-round{
	border-radius:50%;
	outline:0;
	border:0;
	width:50px;
	height:50px;
	margin-left:10px;
	margin-top:5px;
	font-size:20px;
}

</style>
