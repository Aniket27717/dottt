<!doctype html>

<html lang="en">   
 <head>   
  <meta charset="UTF-8">   
  <meta name="viewport" content="width=device-width, initial-scale=1.0">   
  <title>Public Chat</title>   
  <link rel="stylesheet" href="style.css">
 </head>   
 <body>   
  <h2>Public Chat</h2>   
  <input type="text" id="username" placeholder="Enter your name">   
  <div id="chatbox"></div>   
  <input type="text" id="message" placeholder="Type a message"> <button onclick="sendMessage()">Send</button> <button onclick="clearChat()">Clear Chat</button> <!-- Instructions Button --> <button id="instructions-btn">ℹ️</button>   
  <div id="instructions-box">   
   <p><strong>Instructions:</strong></p>   
   <p>1. Long-press a message to unsend.</p>   
   <p>2. Double-tap a message to edit .</p>   
   <p>3. Type your message and press"Send" or Enter.</p>   
   <p>4.Enter your name before sending a message.</p>   
   <p>5. Click "Clear Chat" to delete all messages.</p> <button id="back-btn">Back</button>   
  </div>   
  <script type="module">    
        import { initializeApp } from "https://www.gstatic.com/firebasejs/9.6.1/firebase-app.js";    
        import { getDatabase, ref, push, onChildAdded, remove, update } from "https://www.gstatic.com/firebasejs/9.6.1/firebase-database.js";  const firebaseConfig = {    
        apiKey: "AIzaSy...your_api_key",    
        authDomain: "chat-45809.firebaseapp.com",    
        databaseURL: "https://chat-45809-default-rtdb.firebaseio.com",    
        projectId: "chat-45809",    
        storageBucket: "chat-45809.appspot.com",    
        messagingSenderId: "110882798857",    
        appId: "1:110882798857:web:98ba57db5c40588231a7d8",    
        measurementId: "G-N4TZLZPGCZ"    
    };    const app = initializeApp(firebaseConfig);    
const database = getDatabase(app);    

document.addEventListener("DOMContentLoaded", () => {    
    const storedUsername = localStorage.getItem("username");    
    if (storedUsername) {    
        document.getElementById("username").value = storedUsername;    
    }    
});    

window.sendMessage = function () {    
    const username = document.getElementById("username").value.trim();    
    const message = document.getElementById("message").value.trim();    
        
    if (username === "" || message === "") {    
        alert("Enter a name and message!");    
        return;    
    }    

    localStorage.setItem("username", username);    

    push(ref(database, "public_messages"), {    
        user: username,    
        text: message,    
        timestamp: Date.now()    
    });    

    document.getElementById("message").value = "";    
};    

function formatTime(timestamp) {    
    const date = new Date(timestamp);    
    return `${date.getHours()}:${date.getMinutes()}:${date.getSeconds()}`;    
}    

function loadMessages() {    
    const chatbox = document.getElementById("chatbox");    

    onChildAdded(ref(database, "public_messages"), (snapshot) => {    
        const msg = snapshot.val();    
        const msgElement = document.createElement("p");    

        msgElement.innerHTML = `<strong>${msg.user}:</strong> <span class="msg-text">${msg.text}</span>    
            <span class="timestamp">${formatTime(msg.timestamp)}</span>`;    

        msgElement.setAttribute("data-id", snapshot.key);  

        let lastTap = 0;  
        msgElement.addEventListener("click", function () {  
            let currentTime = new Date().getTime();  
            let tapLength = currentTime - lastTap;  
            if (tapLength < 300 && tapLength > 0) {  
                editMessage(snapshot.key, msgElement.querySelector(".msg-text"), msg.text);  
            }  
            lastTap = currentTime;  
        });  

        msgElement.addEventListener("contextmenu", function (event) {  
            event.preventDefault();  
            confirmDeleteMessage(snapshot.key, msgElement);  
        });  

        chatbox.appendChild(msgElement);  
        chatbox.scrollTop = chatbox.scrollHeight;    
    });    
}    

function editMessage(messageId, msgElement, oldText) {  
    const newText = prompt("Edit your message:", oldText);  
    if (newText !== null && newText.trim() !== "") {  
        const updates = {};  
        updates["public_messages/" + messageId + "/text"] = newText;  
        update(ref(database), updates).then(() => {  
            msgElement.textContent = newText;  
        });  
    }  
}  

function confirmDeleteMessage(messageId, msgElement) {  
    if (confirm("Do you want to unsend this message?")) {  
        remove(ref(database, "public_messages/" + messageId)).then(() => {  
            msgElement.remove();  
        });  
    }  
}  

window.clearChat = function () {    
    if (confirm("Are you sure you want to clear the chat?")) {    
        remove(ref(database, "public_messages"));    
        document.getElementById("chatbox").innerHTML = "";    
    }    
};    

document.getElementById("instructions-btn").addEventListener("click", function() {  
    const box = document.getElementById("instructions-box");  
    box.style.display = box.style.display === "block" ? "none" : "block";  
});  

loadMessages();    
  
document.getElementById("back-btn").addEventListener("click", function() {  
document.getElementById("instructions-box").style.display = "none";

});

</script>   </body></html>
