<script>
    // import {createEventDispatcher} from 'svelte';
    // const dispatch = createEventDispatcher();
</script>

<div>
    <!-- <button on:click|preventDefault={()=>dispatch('btnClick')}> 바로 시작하기 </button> -->
    <button on:click|preventDefault> 바로 시작하기 </button>
</div>

<style>
    button{
        width: 150px;
        height: 40px;
        font-size:15px;
        font-weight: 500;
    }
</style>