<script>
  import svelteLogo from "./assets/svelte.svg";
  import viteLogo from "/vite.svg";
  import Router from "svelte-spa-router";
  import Home from "./routes/Home.svelte";
  import Navigation from "./Navigation.svelte";
  import Footer from "./Footer.svelte";
  import NotFound from "./NotFound.svelte";

  const routes = {
    "/": Home,
    "*" : NotFound,
  };
</script>

<link
  rel="stylesheet"
  href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css"
/>

<Navigation />
<Router {routes} />
<Footer />
