<script>
    let name;
    let belt_color;
    let age;
    let skills = [];

    const submitForm = () => {
        console.log(name, belt_color, age, skills);
    }
</script>

<form class="modal-form" on:submit|preventDefault={submitForm}>
    <input type="text" name="name" id="name" placeholder="Name" bind:value={name}>
    <input type="text" name="belt_color" id="belt_color" placeholder="Belt color" bind:value={belt_color}>
    <input type="number" name="age" id="age" placeholder="Age" bind:value={age}>

    <label for="skills">Skills:</label>
    <div id="skill_set">
        <label for="">Skill 1
            <input type="checkbox" bind:group={skills} value="Walking">
        </label>
        
        <label for="">Skill 2
            <input type="checkbox" bind:group={skills} value="Talking">
        </label>

        <label for="">Skill 3
            <input type="checkbox" bind:group={skills} value="Sprinting">
        </label>

        <label for="">Skill 4
            <input type="checkbox" bind:group={skills} value="Jumping">
        </label>
    </div>  

    <div id="belts">
        <select name="belt_color" id="belt_color" bind:value={belt_color}>
            <option value="Black">Black</option>
            <option value="Orange">Orange</option>
            <option value="Blue">Blue</option>
            <option value="Red">Red</option>
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
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
    }
</style>