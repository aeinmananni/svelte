<script lang="ts">
import {shuffle} from "lodash";
import type {PersonsType} from "./model";
  const cities = ["sari","tehran","Mazandran"];
  let courses =["javascripte","sql","react","svelte"];

  const handelShuffle = () =>{
    courses = shuffle(courses)
  }
  const persons:PersonsType[] = 
  [
     {
        id:1,
        firstName:"AAA",
        lastName:"aaa"
     },
     {
        id:2,
        firstName:"BBB",
        lastName:"bbb"
     },
     {
        id:3,
        firstName:"CCC",
        lastName:"ccc"
     },
  ]

function handlePersonClick(person: PersonsType) {
    console.log(person);
}
</script>

<main class="flex flex-col gap-12">
      <hr/>
      <h1 class="font-bold">List And Ket Course</h1>
      <ul>
        {#each cities as city,index }
            <li>{index + 1} : {city}</li>
        {/each}
      </ul>
                
       <div>
            {#each persons as person}
                 <button  on:click={() => handlePersonClick(person)}>{person.firstName} {person.lastName}</button>
            {/each}
       </div>

       <div class="flex flex-col gap-4">
           {#each courses as course (course) }
               <div class="flex flex-col gap-2">
                   <h2>{course}</h2>
                   <input  placeholder="Provinse" class="border"/>
               </div>
           {/each}
           <button class="bg-blue-500 text-white" on:click={handelShuffle}>OnShuffle</button>
       </div>
</main>