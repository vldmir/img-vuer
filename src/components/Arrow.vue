<template>
  <div>
    <button class="paginate left" :data-state="leftDisable" @click="$emit('prev-slide')">
      <i></i><i></i>
    </button>
    <button class="paginate right" :data-state="rightDisable" @click="$emit('next-slide')">
      <i></i><i></i>
    </button>
  </div>
</template>

<script>
  export default {
    name: "Arrow",
    props: {
      activePrev: {
        type: Boolean,
        default: true,
      },
      activeNext: {
        type: Boolean,
        default: true,
      }
    },
    computed:{
      rightDisable(){
        return this.activeNext?'':'disabled';
      },
      leftDisable(){
        return this.activePrev?'':'disabled';
      }
    }
  }
</script>
