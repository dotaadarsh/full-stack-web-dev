<style>

.todo{
    display: grid;
    grid-template-columns: 2rem 1fr 2rem;
    grid-gap: 0.5rem;
    align-items: center;
    margin: 0 0 0.5rem 0;
    padding: 0.5rem;
    background-color: white;
    border-radius: 8px;
    filter: drop-shadow(2px 4px 6px rgba(0, 0, 0, 0.1));
    transform: translate(-1px, -1px);
    transition: filter 0.2s, transform 0.2s;
}

.todo button{
    width: 2em;
    height: 2em;
    border: none;
    background-color: transparent;
    background-position: 50% 50%;
    background-repeat: no-repeat;
}

.todo input{
    flex: 1;
    padding: 0.5em 2em 0.5em 0.8em;
    border-radius: 3px;
}

button.toggle{
    border: 1px solid rgba(0, 0, 0, 0.2);
    border-radius: 50%;
    box-sizing: border-box;
    background-size: 1em auto;
}

.text{
    position: relative;
    display: flex;
    align-items: center;
    flex: 1;
}

.save{
    position: absolute;
    right: 0;
    opacity: 0;
    background-image:url("https://www.svgrepo.com/show/71047/save.svg");
}

.todo input:focus + .save,
.save:focus {
        transition: opacity 0.2s;
        opacity: 1;
}

.delete {
    background-image:url("https://www.svgrepo.com/show/162728/delete.svg");
    opacity: 0.2;
}

.delete:hover,
.delete:focus{
    transition: opacity 0.2s;
    opacity: 1;
}

/* TODO: uncomment when the API endpoints are available
.done{
    transform: none;
    opacity: 0.4;
    filter: drop-shadow(0 0 1px rgba(0, 0, 0, 0.1));
}
.done .toggle{
    background-image: url("https://www.svgrepo.com/show/326969/checkmark-done-sharp.svg");
}
*/
</style>

<div class ="todo">
    <form action="" method="">
        <input type="hidden" name="done" value=""/>
        <button aria-label="Mark Done/NotDone" class= "toggle"></button> 
    </form>
    
    <form action="" method="" class="text">
        <input type="text"/>
        <button aria-label="Save todo" class="save"></button>
    </form>

    <form action="" method="">
        <button aria-label="Delete todo" class="delete"></button> 
    </form>
</div>