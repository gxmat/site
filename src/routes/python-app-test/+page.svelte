<script>
  import { onMount } from "svelte";

  const url = "http://127.0.0.1:8000/test?a=";
  const max = 10000;
  let random_number = 0;

  onMount(async () => {
    fetch(url + max, {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
      },
    })
      .then((response) => response.json())
      .then((data) => (random_number = data))
      .catch((error) => console.log(error));
  });
</script>

<title>Python App Test</title>

<div class="index">
  <h1>Python App Test</h1>
  <p>This page demonstrates connecting the main website to a Python API</p>
  <p>{random_number} is a random number between 0 and {max}</p>
</div>
