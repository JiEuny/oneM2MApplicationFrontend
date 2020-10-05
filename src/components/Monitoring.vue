<template>
  <div>
    <div class="grid-content bg-purple-light">
      <pre>{{ JSON.stringify(response, null, "\t") }}</pre>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      response: [],
    };
  },
  mounted() {
    axios.get("http://localhost:3000/notify").then((res) => {
      console.log(res.data);
      // alert(res.data)
      this.response = JSON.parse(res.data);
    });
  },
};
</script>

<style scoped>
.bg-purple-light {
  background: #e5e9f2;
  text-align: left;
  margin: 10% 10% 10% 10%;
  min-height: 1000px;
  font-size: 1.5em;
}
</style>