
<script>

let status = "";
const handleSubmit = async data => {
  status = 'Submitting...'
  const formData = new FormData(data.currentTarget)
  const object = Object.fromEntries(formData);
  const json = JSON.stringify(object);

  const response = await fetch("https://api.web3forms.com/submit", {
      method: "POST",
      headers: {
          "Content-Type": "application/json",
          Accept: "application/json",
      },
      body: json
  });
  const result = await response.json();
  if (result.success) {
      console.log(result);
      status = result.message || "Success"
  }
}

</script>
<div class="container">
    <form on:submit|preventDefault={handleSubmit} class="form">
        <input type="hidden" name="access_key" value="97ee4d52-31ba-44a8-a99d-1c3d22695f04">
        <input type="text" name="name" required  placeholder="Your name"/>
        <input type="email" name="email" required placeholder="Your email"/>
        <textarea name="message" required rows="4" placeholder="message"></textarea>
        <button type="submit">submit</button>
    </form>
    <div class="status">{status}</div>
</div>


<style>
    .container {
        margin-block: 1rem;
    }
    .form {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin-inline: 2rem;
        margin-bottom: 2rem;
        font-size: 30px;
    }

    button {
        color: white;
        background-color: black;
        font-family: 'Assistant', sans-serif;
        border-radius: 0.7rem;
        text-transform: uppercase;
        width: 30%;
        padding-block: 0.5rem;
        border: none;
            }

    button:hover {
        background-color: var(--text-yellow);
        color: black;
    }

    input, textarea {
        border: 1px solid rgb(126, 125, 125);
        border-radius: 0.5rem;
        padding: 0.5rem; 
        font-family: 'Assistant', sans-serif;
        max-width: 100%;
        font-size: 20px;
     }

     .status{
        margin-inline: 2rem;
        color: green;
        font-size: 20px;
     }

     @media (min-width: 600px) {
        input, textarea {
            max-width: 50%;
        }

     }
            
</style>