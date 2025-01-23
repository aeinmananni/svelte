<script>

    const compoany = "this is my text";
    const course = "<span>my svelt Code</span>";
    const hack = `<a href="#" onclick="alert('message')">Win prize</a>`;
</script>

<main>
      <button type="button" class="text-rose-600 text-2xl font-bold" onclick={() => alert("message")}>{compoany}</button>
      {@html course}
      <hr/>
      {@html hack}
</main>