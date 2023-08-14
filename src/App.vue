<template>
  <div>
    <h1>This App comsumes data from FastAPIBasic APP</h1>
    <get-data></get-data>
  </div>
</template>

<script>
import GetData from './components/GetData.vue';

export default {
  components: {
    GetData
  }
}
</script>
