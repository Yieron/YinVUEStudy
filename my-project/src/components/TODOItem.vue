<template>
  <div class="TODOItem">
    <ul>
        <li class="item" @click="handleDelete">{{content}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'TODOItem',
  props:['content','index'],
  methods:{
      handleDelete(){
          this.$emit('delete',this.index)
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    .item{
        color: blue
    }
</style>
