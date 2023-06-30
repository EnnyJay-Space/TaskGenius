<template>
  <div class="home">
    <field-add-task/>
    <list-task
      v-if="$store.state.tasks.length"
    />
      
    <!-- </field-add-task> -->
    <no-tasks 
      v-else
    />
    
  </div>
</template>

<script>

  export default {
    name: 'Home',
    
    components:{
      'field-add-task': require('@/components/Todo/FieldAddTask.vue').default,
      'list-task': require('@/components/Todo/ListTasks.vue').default,
      'no-tasks': require('@/components/Todo/NoTasks.vue').default
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
