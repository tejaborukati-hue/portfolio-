<!DOCTYPE html>
<html>
<head>
    <title>AI Chatbot</title>

    <style>

        body{
            font-family: Arial;
            background: #f4f4f4;
            display:flex;
            justify-content:center;
            align-items:center;
            height:100vh;
        }

        .chatbox{
            width:350px;
            background:white;
            border-radius:10px;
            padding:20px;
            box-shadow:

        #messages{
            height:300px;
            overflow-y:auto;
            border:1px solid #ccc;
            padding:10px;
            margin-bottom:10px;
        }

        input{
            width:70%;
            padding:10px;
        }

        button{
            padding:10px;
            background:#2563eb;
            color:white;
            border:none;
            border-radius:5px;
        }

    </style>
</head>

<body>

    <div class="chatbox">

        <h2>AI Chatbot</h2>

        <div id="messages"></div>

        <input type="text" id="userInput" placeholder="Type message">

        <button onclick="sendMessage()">Send</button>

    </div>

    <script>

        function sendMessage(){

            let input = document.getElementById("userInput").value;

            let messages = document.getElementById("messages");

            messages.innerHTML += "<p><b>You:</b> " + input + "</p>";

            let reply = "";

            if(input.toLowerCase().includes("hello")){
                reply = "Hello! How can I help you?";
            }
            else if(input.toLowerCase().includes("name")){
                reply = "I am your AI chatbot.";
            }
            else{
                reply = "Sorry, I am still learning.";
            }

            messages.innerHTML += "<p><b>Bot:</b> " + reply + "</p>";

            document.getElementById("userInput").value = "";

        }

    </script>

</body>
</html>