
<template>
    <div>
      <h2>Received Data:</h2>
      {{ data.msg }}
      <!-- will print error if any -->
      {{ data.message }} 
    </div>
</template>
  
<script>
  import axios from 'axios';
  
  export default {
    data() {
      return {
        data: []
      };
    },
    created() {
      this.fetchData();
    },
    methods: {
      fetchData() {
        axios.get('http://localhost:8000/')
          .then(response => {
            this.data = response.data;
            console.log(this.data)
          })
          .catch(error => {
            console.error('Error fetching data:', error);
            this.data = error;
          });
      }
    }
  }
</script>
  