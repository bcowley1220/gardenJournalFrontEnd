<script>
  let userName;
  let password;
  let data = [];
  const localHost8080 = `http://localhost:8080/testFile`;

  const hitBackend = async () => {
    const response = await fetch(localHost8080);
    data = await response.json();
    console.log(data);
  };
  const submitLoginHandler = () => {
    console.log(`${userName}, ${password}`);
    hitBackend();
  };
</script>

<form>
  <div class="inputWrapper">
    <label for="userName" />
    User Name:
    <input type="text" name="userName" bind:value={userName} maxlength="12" />
  </div>
  <div class="inputWrapper">
    <label for="password" />
    Password:
    <input
      type="password"
      name="password"
      bind:value={password}
      maxlength="128" />
  </div>
  <div class="inputWrapper">
    <button type="button" on:click={submitLoginHandler}>Submit</button>
  </div>
</form>
