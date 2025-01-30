<script lang="ts">
     import style from './style.module.css';
      let state = $state<boolean>(false)
</script>

<main>
    <hr/>
      <h1 class={state ? style.bgSuccess : style.bgError}>Wellcom To Styles Pagew</h1>
      <button onclick={() => state = !state}>ChangeToggle</button>
</main>