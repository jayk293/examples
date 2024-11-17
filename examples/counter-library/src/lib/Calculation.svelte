<script lang="ts">
    import Textfield from '@smui/textfield';

    export let value1 = 0;
    export let value2 = 0;
</script>

<Textfield bind:value={value1} label="Number" type="number" />
<Textfield bind:value={value2} label="Number" type="number" />
<slot {value1} {value2}><p>The sum is {value1 + value2}</p></slot>
