<template>
  <div class="home">
    <list-task
      v-if="$store.state.tasks.length"
    />
      
    <!-- </field-add-task> -->
    <no-tasks 
      v-else
    />
    <button-done-sorting 
      v-if="$store.state.sorting"
    />
  </div>
</template>

<script>

  export default {
    name: 'Home',
    
    components:{
      'list-task': require('@/components/Todo/ListTasks.vue').default,
      'no-tasks': require('@/components/Todo/NoTasks.vue').default,
      'button-done-sorting': require('@/components/Todo/ButtonDoneSorting.vue').default
    }
  }
</script>

<style lang="sass">
  .no-tasks
    position: absolute
    left: 50%
    top: 50%
    transform: translate(-50%, -50%)
    opacity: 0.5
  
</style>
