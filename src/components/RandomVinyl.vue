<template>
    <p>{{dataReturned}}</p>
</template>


<script>
import axios from "axios";

export default {
  data() {
    return {
      dataReturned: [],
      errors: []
    };
  },

  async created() {
    let url = `https://mndi3iv2cb.execute-api.us-east-2.amazonaws.com/default/vinylshuffle`;
    let config = {
      headers: {
        "x-api-key": "5ZnRAbCUT59HeZgkWUxJL5OK0gA1elT59FEEeGPU"
      }
    };

    try {
      const response = await axios.get(url, config);
      this.dataReturned = response
    } catch (e) {
      this.errors.push(e);
    }
  }
  
};
</script>