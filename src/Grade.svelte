<script lang="ts">
	export let consumed: number
  export let total: number
  export let width: number

  const pct = (number: number) :number => number * 100 / total
  const balance: number = total - consumed

  let rootElement: HTMLElement

  rootElement && rootElement.style.setProperty('--width', `${width}px`)
  rootElement && rootElement.style.setProperty('--balance', `${pct(balance)}%`)
  rootElement && rootElement.style.setProperty('--consumed', `${pct(consumed)}%`)

</script>

<div class="chart" bind:this="{rootElement}">
  <div class="chart-data">
    <div class="chart-data-center">
      <p>{ consumed }/{ total }</p>
    </div>
  </div>
</div>

<style lang="stylus">
  .chart
    margin: 0 auto
    width: var(--width)
    height: var(--width)
    padding: 8px
    border-radius: var(--width)
    background: conic-gradient( #079992 var(--consumed), #ff4757 var(--balance), #ff4757 calc(var(--consumed) + var(--balance)), #D5D5D5 calc(var(--consumed) + var(--balance)))
  .chart-data
    width: calc(var(--width) - (8px * 2))
    height: calc(var(--width) - (8px * 2))
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