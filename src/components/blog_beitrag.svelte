<!------------------------------------------------------------------------>
<!---------------------- JAVASCRIPT DER COMPONENTE ----------------------->
<!------------------------------------------------------------------------>
<script>
    export let name; 
    export let beschreibung;
</script>





<!------------------------------------------------------------------------>
<!------------------------- CSS DER COMPONENTE --------------------------->
<!------------------------------------------------------------------------>
<style>
    .container-fluid {
        height: 250px;
        width: 90%;
        max-width: 50rem;
        margin-top: 2%;
        border-radius: 10px;
        background: #e9ecef;
    }
    
    h1 {
        padding: 2%;
        font-size: 40px;
        color: black;
    }
    p {
        padding: 2%;
        color: black;
    }
    button {
        padding: 8px;
        background: green;
        border: 1px solid green;
        border-radius: 5px;
        color: white;
    }

    @media only screen and (max-width: 600px) {
        button {
            padding: 8px;
            margin-top: 10%;
        }
    }
</style>




<!------------------------------------------------------------------------>
<!----------------------------- MARKUP HTML ------------------------------>
<!------------------------------------------------------------------------>
<div class="container-fluid">
    <h1>{name}</h1>
    <p>{beschreibung}</p>
    <p style="float: right"><button>Weiterlesen!</button></p>
</div>    
