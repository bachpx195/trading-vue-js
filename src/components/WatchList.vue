
<template>
    <!-- Main component  -->
    <div id="watch-list" :style="style">
      <table class="table table-dark">
        <thead>
          <tr>
            <th scope="col">#</th>
            <th scope="col">change %</th>
            <th scope="col">24h change</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <th scope="row">BTC</th>
            <td :class="`${info.btc_return_day > 0 ? 'green' : 'red'}`">
              {{ info.btc_return_day }}
            </td>
            <td :class="`${info.btc_return_24h > 0 ? 'green' : 'red'}`">
              {{ info.btc_return_24h }}
            </td>
          </tr>
          <tr>
            <th scope="row">LTC</th>
            
            <td :class="`${info.return_day > 0 ? 'green' : 'red'}`">
              {{ info.return_day }}
            </td>
            <td :class="`${info.return_24h > 0 ? 'green' : 'red'}`">
              {{ info.return_24h }}
            </td>
          </tr>
          <tr>
            <th scope="row">LTC.B</th>
            <td>Larry</td>
            <td>the Bird</td>
          </tr>
        </tbody>
      </table>
    </div>
</template>

<script>

// import _ from "lodash"

export default {
    name: 'WatchList',
    components: {  },
    mixins: [],
    props: {
      width: {
          type: Number,
          default: 800
      },
      height: {
          type: Number,
          default: 421
      },
      info: {}
    },
    data() {
        return {
        }
    },
    computed: {
        style() {
            return 'width: ' + this.$props.width + 'px; height: ' + this.$props.height + 'px'
        },
    },
    mounted() {
    },
    methods: {
    }
}
</script>
<style>
#watch-list {
    background: black;
    bottom: 0;
    right: 0;
    font-size: 15px;
    color: red;
    height: auto;
}
.green {
  background: green;
  color: white
}
</style>
