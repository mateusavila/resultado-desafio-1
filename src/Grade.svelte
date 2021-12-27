<script lang="ts">
  import { onMount } from 'svelte'
	export let consumed: number
  export let total: number
  export let width: number

  const pct = (number: number) :number => number * 100 / total

  onMount ( async() => {
    console.log(consumed, total, width)
    console.log(pct(consumed))
  })
</script>

<div class="chart">
  <div class="chart-data">
    <div class="chart-data-center">
      <p>{ consumed }/{ total }</p>
    </div>
  </div>
</div>

<style lang="stylus">
  .chart
    margin: 0 auto 30px
    width: var(--width)
    height: var(--width)
    padding: 5px
    border-radius: var(--width)
    background: conic-gradient( #6D47DB var(--consumed), #F261FF var(--balance), #F261FF calc(var(--consumed) + var(--balance)), #D5D5D5 calc(var(--consumed) + var(--balance)))
  .chart-data
    width: calc(var(--width) - (5px * 2))
    height: calc(var(--width) - (5px * 2))
    background: #fff
    border-radius: 100%
    position: relative
    top: 0
    left: 0
  .chart-data-center
    position: absolute
    display: flex
    align-items: center
    justify-content: center
    width: 100%
    height: 100%
    p
      text-align: center
      margin: 0
      color: #404040
      font-size: 20px
      line-height: 1
      font-weight: bold
</style>