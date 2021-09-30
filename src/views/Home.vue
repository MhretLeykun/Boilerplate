<template>
  <div>Home</div>
</template>
<script>
import axios from 'axios';
export default {
  data() {
    return {
      trendingGiphies: null,
    };
  },
  mounted() {
    this.getTrendingGiphies();
  },
  methods: {
    async getTrendingGiphies() {
      try {
        axios
          .get(
            'https://api.giphy.com/v1/gifs/trending?api_key=dv7bOJvb8GOZ0Y5W6l2coTs9rt9i1MZM'
          )
          .then((response) => {
            console.log(response.data.data);
          });
      } catch (error) {
        console.log(error);
      }
    },
  },
};
</script>
