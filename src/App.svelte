<script lang="ts">
  //  import Counter from "./lib/Counter.svelte";
  import { TextCompany } from "./components/text";
  import { CommunicationProperty } from "./components/communication-property";
  import {AddStyle} from './components/add-style';
  import { Conditions } from "./components/condition";
  import { ListAndKey } from "./components/list-key";
  import {Event} from "./components/event";
  import {FormHandeling} from './components/form-handeling';
</script>
<main>
  <div class="p-2 flex flex-col gap-3">

    <!-- <TextCompany/>
    <CommunicationProperty/>
    <AddStyle/>
    <Conditions/>
    <ListAndKey/>
    <Event/> -->
    <FormHandeling/>
  </div>
</main>