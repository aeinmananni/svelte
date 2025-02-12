<script lang="ts">
    import type {FormTypes} from './model';

    let formState:FormTypes = {
        firstName:"",
        lastName:"",
        userName:"",
        password:"",
        provinse:"",
        skills:[]
    }

    const handelSubmit = (e: Event) => {
         e.preventDefault();
         console.log(formState)
    }
</script>

<main>
    <hr/>

 <form onsubmit={handelSubmit} class="flex flex-col gap-3">
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
    <button type="submit">OnSubmit</button>
 </form>
</main>