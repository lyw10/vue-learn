<template>
  <div class="fliters">
        <span class="fliter active">全部</span>
        <span class="fliter">已完成</span>
        <span class="fliter">未完成</span>
      </div>
</template>

<script>
export default {
    name:"todofliter",
}
</script>

<style>
.fliters{
  display: flex;
  justify-content: start;
  color: #c0c2ce;
  font-size: 14px;
  cursor: pointer;
  margin-bottom: 20px;
}

.fliter{
  margin-right: 14px;
  transition: all .8s;
}

.active{
  color: #6b729c;
  transform: scale(1.2);
}
</style>