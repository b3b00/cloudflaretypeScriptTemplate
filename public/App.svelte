<script lang="ts">

    
    import Router from 'svelte-spa-router'
    

    import C1 from "./C1.svelte";    
    import C2 from "./C2.svelte";
    import C3 from "./C3.svelte";
    import Home from "./Home.svelte"; 

    const routes = {
        // Exact path
        
        // Using named parameters, with last being optional
        '/c1/:message': C1,
        '/c2/:message': C2,
        '/C3/:message': C3,
        '*': Home,
    }
    

</script>

<div style="display:flex;flex-direction:column">
    <div style="display:flex;flex-direction:row">
        <a href="#/C1/component1%20is%20in%20the%20place">C1</a>
        <a href="#/C2/component2%20is%20in%20the%20place">C2</a>
        <a href="#/C3/component3%20is%20in%20the%20place">C3</a>
        <a href="/test">TEST</a>
    </div>
    <hr/>
    <div>
        <Router {routes}/> 
    </div>
    <hr/>
    <div>
        <C1 message="this is static C1" params="{{}}"></C1>
    </div>
</div>