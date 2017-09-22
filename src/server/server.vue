<template>
  <div>
    <li
    style="cursor: pointer"
    class="list-group-item"
    v-for="server in servers">
    Server #{{ server.id }}
  </li>
</div>
</template>
<script>
export default {
  data () {
    return {
      servers: [
        {
          id:1 , status:'online',
        },
        {
          id:2 , status:'offline',
        },
        {
          id:3 , status:'unknow',
        }
      ]
    }
  }
}
</script>
<style>

</style>