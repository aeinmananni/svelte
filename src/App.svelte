<script lang="ts">
  //  import Counter from "./lib/Counter.svelte";
  // import { TextCompany } from "./components/text";
  // import { CommunicationProperty } from "./components/communication-property";
  // import {AddStyle} from './components/add-style';
  // import { Conditions } from "./components/condition";
  // import { ListAndKey } from "./components/list-key";
  // import {Event} from "./components/event";
  // import {FormHandeling} from './components/form-handeling';
  let firstName = "aein";
  let lastName = "mananni";
  $:fullName = `${firstName} ${lastName}`; // اعلان واکنش پذیر

  let items = [
       {
         id:1,
         title:"TV1",
         price:900
       },
       {
         id:1,
         title:"TV2",
         price:400
       },
       {
         id:1,
         title:"TV3",
         price:700
       },
  ]
  $:pricing = `${JSON.stringify(items.reduce((total,current) => total + current.price,0))}`



$:{
     const greet = `${firstName} ${lastName}`;
     console.log(greet)
}
</script>
<main>
  <div class="p-2 flex flex-col gap-3">
    <button on:click={() => items = [...items,{id:4,title:"TV5",price:1540}]}>Add Items</button>
   <h1>{firstName} {lastName}</h1>
   اعلان واکنش پذیر⬇
   <h1>{fullName}</h1>
   <h2>Pricing : {pricing}</h2>
    <!-- <TextCompany/>
    <CommunicationProperty/>
    <AddStyle/>
    <Conditions/>
    <ListAndKey/>
    <Event/> -->
    <!-- <FormHandeling/> -->
  </div>
</main>