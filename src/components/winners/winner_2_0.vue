<template>
  <div class="winner">
    Beta 1.0 - Alpha
    <button class="common" v-if="!expanded && !mobile" @click="expanded = true">&#11167</button>
    <button class="common" v-if="expanded && !mobile" @click="expanded = false">&#11165</button>
    <button class="common" v-if="!expanded && mobile" @click="expanded = true">i</button>
    <button class="common" v-if="expanded && mobile" @click="expanded = false">x</button>
    <div class="detail-winner" :class="!expanded ? 'detail-winner-hidden' : ''">
      <div class="detail-item">
        <div class="detail-label">Winner:</div>
        <div class="detail-content">Alpha (Team)</div>
      </div>
      <div class="detail-item">
        <div class="detail-label">Team members:</div>
        <div class="detail-content">Ramsus, Eloxor, Blutwolf, hedgeh0g</div>
      </div>
      <div class="detail-item">
        <div class="detail-label">Duration:</div>
        <div class="detail-content">27 Days</div>
      </div>
      <div class="detail-item">
        <div class="detail-label">End Date:</div>
        <div class="detail-content">27.11.2019</div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name: 'winner_2_0',
    components: {},
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

<style scoped>

  .winner {
    margin-bottom: 10px;
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

  @keyframes appear {
    from {
      height: 0
    }
    to {
      height: 114px
    }
  }

  @keyframes disappear {
    from {
      height: 114px;
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
      top: 80px;
      height: 80%;
    }

    @keyframes appear {
      from {
        height: 0
      }
      to {
        height: 178px
      }
    }
  }

</style>
