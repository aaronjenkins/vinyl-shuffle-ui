<template>
    <img v-bind:src="dataReturned.data.body.cover.file.url" width="300" height="300"> 
    <p>{{dataReturned.data.body.properties.Title.title[0].plain_text}}</p>
    <p>{{dataReturned.data.body.properties.Artist.select.name}}</p>
    <p>{{dataReturned.data.body.properties["Release Year"].number}}</p>
    <p>{{dataReturned.data.body.properties.Genre.select.name}}</p>
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
    let url = `https://4175a2gyz6.execute-api.us-east-2.amazonaws.com/default/vinylshuffle`;
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