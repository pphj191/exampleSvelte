<script>
    import InputTemplate from "./InputTemplate.svelte";
    import Button from "../lib/Button.svelte";
    import { dev } from "../lib/store"
    
    $dev=0;
    function scrollIntoView() {
		const el = document.querySelector('.inputTemplate');
		if (!el) return;
    el.scrollIntoView({
      behavior: 'smooth'
    });
  }
</script>

<div class="home {$dev?'dev':''}">
    <div class="mainContainer {$dev?'dev':''}">
        <h1>2023</h1>
        <h2>전화 여론조사</h2>
        <p>전화기반으로 다수에게 빠르게 여론조사를 할 수 있습니다</p>
        <Button on:click={scrollIntoView} />
    </div>
</div>
<!-- 실제 여론조사 페이지 -->
<div class="inputTemaplate">
    <InputTemplate />
</div>


<style>
    *{
        font-family: sans-serif;
    }
    .home {
        height: 800px;
        width: 100%;
        position: relative;
        /* opacity:0.1; */
        z-index: 1;
    }
    .home::after {
        height: 800px;
        width: 100%;
        content: "Hello";
        position: absolute;
        background: url("../assets/subway.jpg");
        background-attachment: fixed;
        background-size: cover;
        opacity: 0.3;
        z-index: -1;
        top: 0;
        left: 0;
    }
    .mainContainer {
        position: relative;
        margin: 0 auto;
        padding: 20px;
        max-width: 700px;
        height: 880px;
    }
    .home h1 {
        position: relative;
        font-size: 70px;
        font-weight: 700;
        line-height: 110%;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
            sans-serif;
        margin-top: 200px;
    }
    .home h2 {
        position: sticky;
        top: 350px;
        /* left: 500px; */
        font-size: 50px;
        font-weight: 700;
        line-height: 110%;
        font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS",
            sans-serif;
    }
    .home p {
        margin: 10px 0 30px;
    }
    .dev {
        border: solid rgba(255, 0, 0, 0.5);
    }
    button{
        width: 150px;
        height: 40px;
        font-size:15px;
        font-weight: 500;
    }
</style>
