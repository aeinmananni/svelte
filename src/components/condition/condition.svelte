<script lang="ts">
    let number = $state<number>(0)
</script>

<main>
    <hr/>
     {#if number === 0 }
         <h1>Number is zero</h1>
         {:else if number < 0}
            <h1>number is Negative</h1>
         {:else}
           <h1>{number}</h1>
     {/if}
     <button class="bg-green-500 p-3" onclick={() => number += 1}>+</button>
     <button class="bg-red-500 p-3" onclick={() => number -= 1}>-</button>
</main>