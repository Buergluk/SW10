<script>
    let name = "";
    let email = "";
    let problemTitle = "";
    let problemDescription = "";

    function handleSubmit(event) {
        event.preventDefault();
        const formData = {
            name,
            email,
            problemTitle,
            problemDescription,
        };
        console.log(formData);
        // Hier kannst du die Formulardaten weiterverarbeiten, z.B. an einen Server senden
    }
</script>

<div class="text-box">
    <h1>Kontakt</h1>
    <p>
        Wir freuen uns, von dir zu hören! Ob du Fragen zu unseren Berghütten, zur
        Buchung oder zu besonderen Wünschen hast – wir sind hier, um dir zu helfen.
    </p>
    <h2>So erreichst du uns:</h2>
    <p>📧 E-Mail: info@example.ch</p> 
    <p>📞 Telefon: +49 123 456 7890</p>
    <h2>Postadresse:</h2>
    <p>ShareYourHut GmbH Bergstraße 12 12345 Alpenstadt</p>
    <h2>Oder nutze unser Kontaktformular:</h2>
    <form on:submit={handleSubmit}>
        <div class="form-group">
            <label for="name">Name:</label>
            <input type="text" id="name" bind:value={name} />
        </div>
        <div class="form-group">
            <label for="email">Email:</label>
            <input type="email" id="email" bind:value={email} />
        </div>
        <div class="form-group">
            <label for="problemTitle">Problemtitel:</label>
            <input type="text" id="problemTitle" bind:value={problemTitle} />
        </div>
        <div class="form-group">
            <label for="problemDescription">Problembeschreibung:</label>
            <textarea id="problemDescription" bind:value={problemDescription}></textarea>
        </div>
        <button type="submit">Absenden</button>
    </form>
</div>

<style>
    .text-box {
        background-color: rgba(255, 255, 255, 0.8);
        width: 50%;
        height: 100vh;
        margin: 0;
        padding: 20px;
        overflow: auto; /* Falls der Inhalt größer als die Box ist */
    }

    .form-container {
        background-color: white;
        color: black;
        border-radius: 8px;
        padding: 20px;
        margin: 20px 0;
        max-width: 600px;
    }

    form {
        display: flex;
        flex-direction: column;
        gap: 10px;
        max-width: 600px;
        margin: 0;
    }

    .form-group {
        display: flex;
        align-items: center;
    }

    .form-group label {
        flex: 1;
        margin-right: 10px;
    }

    .form-group input,
    .form-group textarea {
        flex: 2;
        background-color: transparent;
        border: 1px solid #ccc;
        padding: 10px;
        font-size: 16px;
        width: 100%;
        box-sizing: border-box;
        color: white !important;
    }

    .form-group textarea {
        resize: vertical;
    }

    button {
        padding: 10px;
        font-size: 16px;
        cursor: pointer;
        background-color: black;
        color: white;
    }
</style>
