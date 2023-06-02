
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
    <form onsubmit="sendEmail(); reset(); return false;">
        <input type="text" placeholder="Your name" required>
        <input type="email" placeholder="Your email adress" required>
        <textarea rows="4" placholder="What can I do for you ?"></textarea>
        <button type="submit">submit</button>
</form>

</div>