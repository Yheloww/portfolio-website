
<script>
    function sendEmail(){
        Email.send({
    Host : "smtp.elasticemail.com",
    Username : "username",
    Password : "password",
    To : 'them@website.com',
    From : "you@isp.com",
    Subject : "This is the subject",
    Body : "And this is the body"
    }).then(
    message => alert(message)
    );
    }

</script>




<div class="container">
    <form  class="form" onsubmit="sendEmail(); reset(); return false;">
        <input class="input"type="text" placeholder="Your name" required>
        <input class="input"type="email" placeholder="Your email adress" required>
        <textarea class="input"rows="4" placholder="What can I do for you ?"></textarea>
        <button type="submit">submit</button>
</form>

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
    }

    button {
        color: white;
        background-color: black;
        font-family: 'Assistant', sans-serif;
        border-radius: 1rem;
        text-transform: uppercase;
        width: 30%;
        padding-block: 0.5rem;
        border: none;
            }

    button:hover {
        background-color: var(--text-yellow);
        color: black;
    }

    .input {
        border: 1px solid rgb(126, 125, 125);
        border-radius: 0.5rem;
        padding: 0.5rem; 
        font-family: 'Assistant', sans-serif;
        max-width: 100%;
     }

     @media (min-width: 600px) {
        .input {
            max-width: 50%;
        }

        input {
            max-width: 25%;
        }

     }
            
</style>