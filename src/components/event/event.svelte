<script lang="ts">
   let count  = 0;

   const handelIncrement = (stepSize:number) => {
    count += stepSize;
   }
 </script>   
 
 <main>
  <hr/>   
   <div class="flex items-center gap-2">

     <span>{count}</span>
     <button class="bg-green-500 p-2 rounded-md" on:click={() => handelIncrement(5)}>+</button>
     <button class="bg-red-500 p-2 rounded-md" on:click={() => count--}>-</button>
   </div>
 </main>