<script lang="ts">
    import Textfield from '@smui/textfield';
    import Tab, { Label } from '@smui/tab';
    import TabBar from '@smui/tab-bar';
    import Calculation from './Calculation.svelte'



    export let active = "1";

</script>

<TabBar tabs={['1', '2', '3']} let:tab bind:active>
    <!-- Note: the `tab` property is required! -->
    <Tab {tab}>
      <Label>{tab}</Label>
    </Tab>
  </TabBar>
 
  {#if active === '1'}
  <Calculation let:value1 let:value2>
    <p>{value1} plus {value2} is {value1 + value2}</p>
  </Calculation>  {:else if active === '2'}
  <Calculation let:value1 let:value2>
    <p>{value1} minus {value2} is {value1 - value2}</p>
  </Calculation>
  {:else if active === '3'}
  <Calculation let:value1 let:value2>
    <p>{value1} to the power of {value2} is {Math.pow(value1, value2)}</p>
  </Calculation>

  {/if}




