<script>
    import { createEventDispatcher } from "svelte";
    
    let dispatch = createEventDispatcher();

    let name;
    let belt_color;
    let age;
    let weapon;
    let skills = [];

    const submitForm = () => {
        const person = {
            name,
            belt_color,
            age,
            skills,
            weapon,
            id: Math.random()
        };

        dispatch('addPerson', person);

    };
</script>

<form class="modal-form" on:submit|preventDefault={submitForm} autocomplete="off">
    <input type="text" name="name" id="name" placeholder="Name" bind:value={name}>
    <input type="text" name="belt_color" id="belt_color" placeholder="Belt color" bind:value={belt_color}>
    <input type="number" name="age" id="age" placeholder="Age" bind:value={age}>

    <label for="skills">Skills:</label>
    <div id="skill_set">
        <label for="">Stealth
            <input type="checkbox" bind:group={skills} value="Stealth">
        </label>
        
        <label for="">Talking
            <input type="checkbox" bind:group={skills} value="Talking">
        </label>

        <label for="">Sprinting
            <input type="checkbox" bind:group={skills} value="Sprinting">
        </label>

        <label for="">Jumping
            <input type="checkbox" bind:group={skills} value="Jumping">
        </label>
    </div>  

    <div id="weapons">
        <select name="weapon_class" id="weapon_class" bind:value={weapon}>
            <option selected disabled>Choose your weapon</option>
            <option value="Claymore">Claymore</option>
            <option value="Sword">Sword</option>
            <option value="Spear">Spear</option>
            <option value="Gauntlets">Gauntlets</option>
        </select>
    </div>

    <button>Add person</button>
</form>

<style>
    .modal-form
	{
		display: flex;
		flex-direction: column;
	}

    #skill_set
    {
        margin: 20px 0px 20px 0px;
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
    }

    #weapons
    {
        margin: 20px 0px 20px 0px;
    }
</style>