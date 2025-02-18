<script lang="ts">
    import type {FormTypes} from './model';

    let formState:FormTypes = {
        firstName:"",
        lastName:"",
        userName:"",
        password:"",
        provinse:"",
        skills:[],
        remoteWork:false,
        favirites:[],
        yearsOfExperience:""
    }

    const handelSubmit = () => {
         console.log(formState)
    }
</script>

<main>
    <hr/>

 <form on:submit|preventDefault={handelSubmit} class="flex flex-col gap-3">
    <div class="flex flex-col gap-2">
        <label for="firstName">firstName</label>
        <input bind:value={formState.firstName} type="text" id="firstName" class="border outline-none"/>
    </div>

    <div class="flex flex-col gap-2">
        <label for="lastName">lastName</label>
        <input bind:value={formState.lastName}  type="text" id="lastName" class="border outline-none"/>
    </div>


    <div class="flex flex-col gap-2">
        <label for="userName">userName</label>
        <input bind:value={formState.userName}  type="text" id="userName" class="border outline-none"/>
    </div>


    <div class="flex flex-col gap-2">
        <label for="password">password</label>
        <input bind:value={formState.password} type="text" id="password" class="border outline-none"/>
    </div>


    <div class="flex flex-col gap-2">
        <label for="provinse">Provinse</label>
        <select class="border p-1 outline-none" bind:value={formState.provinse} id="provinse">
            <option value="">Selected Provinse</option>
            <option value="farse">Farse</option>
            <option value="mozandaran">Mozandaran</option>
            <option value="tehran">Tehran</option>
        </select>
    </div>


    <div class="flex flex-col gap-2">
        <label for="skills">Skills</label>
        <select class="border p-1 outline-none" bind:value={formState.skills} id="skills" multiple>
            <option value="">Selected skills</option>
            <option value="javascripte">javascripte</option>
            <option value="sql server">sql server</option>
            <option value="Svelte">Svelte</option>
        </select>
    </div>


    <div id="favorites" class="flex  gap-2 w-max">
        <label for="remoteWork">Open to remote work ?</label>
        <input bind:checked={formState.remoteWork} type="checkbox" id="remoteWork" class="border outline-none"/>
    </div>



    <div  class="flex flex-col">
        <label for="favorites">Favorites</label>
        <div class="flex  gap-2 w-max">
            <label for="sports">Sports</label>
            <input bind:group={formState.favirites} type="checkbox" value="sports" id="sports" class="border outline-none"/>
        </div>   
        <div class="flex  gap-2 w-max">
            <label for="music">music</label>
            <input bind:group={formState.favirites} type="checkbox" id="music" value="music" class="border outline-none"/>
        </div>   
        <div class="flex  gap-2 w-max">
            <label for="movie">movie</label>
            <input bind:group={formState.favirites} type="checkbox" id="movie" value="movie" class="border outline-none"/>
        </div>   
     </div>



    <div  class="flex flex-col">
        <label for="favorites">Years of Experience</label>
        <div class="flex  gap-2 w-max">
            <label for="0-2">0-2</label>
            <input bind:group={formState.yearsOfExperience} type="radio" value="0-2" id="0-2" class="border outline-none"/>
        </div>   
        <div class="flex  gap-2 w-max">
            <label for="2-4">2-4</label>
            <input bind:group={formState.yearsOfExperience} type="radio" id="2-4" value="2-4" class="border outline-none"/>
        </div>   
        <div class="flex  gap-2 w-max">
            <label for="3-6">3-6</label>
            <input bind:group={formState.yearsOfExperience} type="radio" id="3-6" value="3-6" class="border outline-none"/>
        </div>   
     </div>

    <button type="submit">OnSubmit</button>
 </form>
</main>