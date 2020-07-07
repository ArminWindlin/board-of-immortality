<template>
  <div class="window-container">
    <div class="empty window">
      <div class="title">World Winners</div>
      <winner_3_13></winner_3_13>
      <winner_3_12></winner_3_12>
      <winner_3_11></winner_3_11>
      <winner_3_10></winner_3_10>
      <winner_3_9></winner_3_9>
      <winner_3_8></winner_3_8>
      <winner_3_7></winner_3_7>
      <winner_3_6></winner_3_6>
      <winner_3_5></winner_3_5>
      <winner_3_4></winner_3_4>
      <winner_3_3></winner_3_3>
      <winner_3_2></winner_3_2>
      <winner_3_1></winner_3_1>
      <winner_3_0></winner_3_0>
      <winner_2_1></winner_2_1>
      <winner_2_0></winner_2_0>
      <winner_1_1></winner_1_1>
      <winner_1_0></winner_1_0>
    </div>
  </div>
</template>

<script>
  import Winner_1_0 from "./winners/winner_1_0";
  import Winner_1_1 from "./winners/winner_1_1";
  import Winner_2_0 from "./winners/winner_2_0";
  import Winner_2_1 from "./winners/winner_2_1";
  import Winner_3_0 from './winners/winner_3_0';
  import Winner_3_1 from './winners/winner_3_1';
  import Winner_3_2 from './winners/winner_3_2';
  import Winner_3_3 from './winners/winner_3_3';
  import Winner_3_4 from './winners/winner_3_4';
  import Winner_3_5 from './winners/winner_3_5';
  import Winner_3_6 from './winners/winner_3_6';
  import Winner_3_7 from './winners/winner_3_7';
  import Winner_3_8 from './winners/winner_3_8';
  import Winner_3_9 from './winners/winner_3_9';
  import Winner_3_10 from './winners/winner_3_10';
  import Winner_3_11 from './winners/winner_3_11';
  import Winner_3_12 from './winners/winner_3_12';
  import Winner_3_13 from './winners/winner_3_13';

  export default {
    name: 'winner-board',
    components: {
      Winner_3_13,
      Winner_3_12,
      Winner_3_11,
      Winner_3_10,
      Winner_3_9,
      Winner_3_8,
      Winner_3_7,
      Winner_3_6,
      Winner_3_5,
      Winner_3_4,
      Winner_3_3, Winner_3_2, Winner_3_1, Winner_3_0, Winner_1_0, Winner_1_1, Winner_2_0, Winner_2_1},
    props: [],
    data() {
      return {
        expanded: false
      }
    },
    computed: {
      mobile: () => {
        return window.mobile;
      }
    },
    methods: {},
    beforeMount() {
    }
  }
</script>

<!--<style scoped src="./field.css"></style>-->
<style scoped>
  .empty {
    background: url(../assets/background3.png) center;
    height: 70%;
    left: 50%;
    top: 150px;
    margin-left: -40vw;
    position: fixed;
    border-radius: 10px;
    box-shadow: 0 0 10px 4px rgba(255, 255, 255, 0.5);
    overflow: auto;
    color: #BEA141;
    padding: 0 20px;
  }

  .title {
    margin: 10px 0 20px 0;
    font-weight: bold;
    font-size: 20px;
  }

  .common {
    background: #BEA141;
    color: white;
    height: 20px;
    width: 20px;
    line-height: 10px;
  }

  .detail-winner {
    background: rgba(255, 255, 255, 0.1);
    margin: 0 20px;
    padding: 5px 0;
    border-radius: 5px;
    overflow: hidden;
    animation: appear 1s;
  }

  .detail-winner-hidden {
    display: none;
    height: 0;
  }

  .detail-item {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
    margin: 10px;
  }

  .detail-label {
    display: inline;
    width: 45%;
    text-align: left;
  }

  .detail-content {
    display: inline;
    width: 45%;
    text-align: left;
  }

  #final-report {
    background: url(../assets/final-report.png) center no-repeat;
    background-size: contain;
    margin: 10px auto;
    width: 800px;
    height: 325px;
    border-radius: 5px;
  }

  @keyframes appear {
    from {
      height: 0
    }
    to {
      height: 423px
    }
  }

  @keyframes disappear {
    from {
      height: 423px;
      display: block
    }
    to {
      height: 0;
      display: none
    }
  }

  @media (max-width: 1100px) {
    #final-report {
      display: none;
    }
  }

  @media (max-width: 768px) {
    .empty {
      position: fixed;
      top: 80px;
      left: 50%;
      transform: translateX(-50%);
      margin: 0
    }

    @keyframes appear {
      from {
        height: 0
      }
      to {
        height: 104px
      }
    }
  }

</style>
