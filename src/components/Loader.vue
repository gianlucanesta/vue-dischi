<template>

<div class="lds-dual-ring"></div>
   
</template>

<script>
export default {
    name: 'Loader',
}
</script>

<style scoped lang="scss">
@import '../style/variables.scss';

.lds-dual-ring {
  margin-top: 40vh;
  display: inline-block;
  width: 100px;
  height: 100px;
}
.lds-dual-ring:after {
  content: " ";
  display: block;
  width: 80px;
  height: 80px;
  margin: 8px;
  border-radius: 50%;
  border: 6px solid #fff;
  border-color: #fff transparent #fff transparent;
  animation: lds-dual-ring 1.2s linear infinite;
}
@keyframes lds-dual-ring {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
</style>