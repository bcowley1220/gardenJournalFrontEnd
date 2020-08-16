<script>
  export let journalEntryForm;
  export let entryIntro;
  export let entryDescription;
</script>

<style>

</style>

<form id="journalEntryForm">
  <div class="inputWrapper">
    <label for="entryDate" />
    Journal Entry Date:
    <input type="date" name="entryDate" bind:value={journalEntryForm} />
  </div>
  <div class="inputWrapper">
    <label for="entryInfo" />
    Short Description:
    <input
      type="text"
      name="entryIntro"
      bind:value={entryIntro}
      maxlength="128" />
  </div>
  <div class="inputWrapper">
    <label for="entryDescription" />
    Full Description:
    <textarea
      type="date"
      name="entryDescription"
      rows="10"
      cols="40"
      bind:value={entryDescription} />
  </div>
</form>
