<script lang="ts">
  //  import Counter from "./lib/Counter.svelte";
  import { TextCompany } from "./components/text";
  import { CommunicationProperty } from "./components/communication-property";
  import {AddStyle} from './components/add-style';
  import {Conditions} from './components/condition';
  import Condition from "./components/condition/condition.svelte";
</script>
<main>
  <div class="p-2 flex flex-col gap-3">

    <TextCompany/>
    <CommunicationProperty/>
    <AddStyle/>
    <Condition/>
  </div>
</main>