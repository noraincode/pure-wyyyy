<template>
  <div class="list-box">
    <div class="list-bar">
    </div>
    
  </div>
</template>

<style lang="scss" scoped>
.list-box {
    position: relative;
    float: left;
    width: 400px;
    height: 480px;
    overflow: hidden;
}
.list-bar {
    position: relative;
    z-index: 2;
    height: 50px;
    background-color: rgba(255,255,255,.95);
    border-bottom: solid 1px rgba(0,0,0,0);
    box-shadow: 0 0 8px rgba(0,0,0,.12);
}
</style>
