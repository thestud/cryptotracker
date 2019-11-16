<template>
  <div id="app">
    <header>
      <h1>This is Crypto Tracker! SPA</h1>
    </header>
    <main>
      <div id="chartdiv" style="width: 100%; height: 400px;"></div>
    </main>
  </div>
</template>
<script>
  import axios from 'axios'
  export default {
    data () {
      return {
        posts: [],
        errors: []
      }
    },

    created() {
      axios.get('http://localhost:4000/cryptos')
      .then(response => {
        // JSON responses are automatically parsed.
        this.posts = response.data

        AmCharts.makeChart("chartdiv",
            {
                "type": "pie",
                "titleField": "Name",
                "valueField": "Percentage",
                "dataProvider": this.posts
            }
        );

      })
      .catch(e => {
        this.errors.push(e)
      })
    } // created

  } // export default
</script>
