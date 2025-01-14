<script lang="ts">
  let count: number = $state(0)
  const increment = () => {
    count += 1
  }
  const decrement = () =>{
     count -= 1
  }
</script>
<div class="flex gap-5">

  <button class="bg-green-500 text-white" onclick={increment}>
    Increment
  </button>
   <h1>{count}</h1>
  <button class="bg-red-500 text-white" onclick={decrement}>
     decrement
  </button>
</div>