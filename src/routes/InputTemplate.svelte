<script>
    import { dev } from "../lib/store"
    let num=1;
    let questions="";
    
</script>


<div class="inputTemplate {$dev?'dev':''}">
    <!-- <p>input</p> -->
    <div class="mainContainer {$dev?'dev':''}">
        <h1>몇명의 여론을 조사할 예정이신가요? </h1>
        <input bind:value={num}>
        <h1>어떤게 궁금하세요? </h1>
        <input bind:value={questions}>
    </div>
</div>

<style>
    .inputTemplate{
        height: 800px;
        width: 100%;
        position: relative;

    }
    .mainContainer{
        position: relative;
        height: 400px;
        max-width: 700px;
        padding: 20px;
        margin: 150px auto 0;
    }
    h1{
        margin: 25px 0 15px;
        font-size: medium;
    }
    .dev{
        border: solid rgba(255, 0, 0, .5);
    }
</style>