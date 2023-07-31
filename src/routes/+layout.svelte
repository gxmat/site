<script lang="ts">
  import "../assets/css/app.css";
  import { base } from "$app/paths";
</script>

<nav>
  <a href="{base}/">Home</a>
  <a href="{base}/about">About</a>
  <a href="{base}/python-app-test">Python App Test</a>
</nav>

<slot />
