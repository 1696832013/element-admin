<template>
  <div class="app-container">
    <switch-roles @change="handleRolesChange" />
    <list-test />
  </div>
</template>

<script>
import SwitchRoles from './components/SwitchRoles'
import ListTest from '@/views/test/index.vue'
export default {
  name: 'PagePermission',
  components: { ListTest, SwitchRoles },
  methods: {
    handleRolesChange() {
      this.$router.push({ path: '/permission/index?' + +new Date() })
    }
  }
}
</script>
