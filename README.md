<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Contact Form</title>
  <style>
    /* Background */
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #6a11cb 0%, #2575fc 100%);
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    /* Card */
    .contact-card {
      background: white;
      padding: 30px;
      border-radius: 15px;
      box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
      width: 350px;
      text-align: center;
    }

    .contact-card h2 {
      margin-bottom: 15px;
      color: #333;
    }

    .contact-card p {
      font-size: 14px;
      color: #666;
      margin-bottom: 20px;
    }

    /* Inputs */
    .contact-card input, 
    .contact-card textarea {
      width: 100%;
      padding: 12px;
      margin: 8px 0;
      border: 1px solid #ddd;
      border-radius: 8px;
      font-size: 14px;
    }

    textarea {
      resize: none;
      height: 100px;
    }

    /* Button */
    .contact-card button {
      background: #2575fc;
      color: white;
      border: none;
      padding: 12px;
      width: 100%;
      border-radius: 8px;
      font-size: 16px;
      cursor: pointer;
      margin-top: 10px;
    }

    .contact-card button:hover {
      background: #1a5ed8;
    }
  </style>
</head>
<body>

  <div class="contact-card">
    <h2>📧 Contact Me</h2>
    <p>Fill in your details and send me a message via Gmail.</p>

    <input type="text" id="name" placeholder="Your Full Name" required>
    <input type="email" id="email" placeholder="Your Email" required>
    <textarea id="message" placeholder="Write your message here..." required></textarea>

    <button onclick="sendEmail()">Send via Gmail</button>
  </div>

  <script>
    function sendEmail() {
      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const message = document.getElementById('message').value;

      if (!name || !email || !message) {
        alert("Please fill out all fields.");
        return;
      }

      const subject = "New Message from " + name;
      const body = Name: ${name}%0D%0AEmail: ${email}%0D%0A%0D%0AMessage:%0D%0A${message};

      // change this to your Gmail address
      const mailto = mailto:akosiwreckertaba@gmail.com?subject=${subject}&body=${body};
      window.location.href = mailto;
    }
  </script>

</body>
</html>
