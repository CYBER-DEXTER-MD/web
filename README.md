<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CYBER DEXTER Official</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap');
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        body {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            background-image: url("https://i.ibb.co/VBYx2c7/pexels-pedro-figueras-202443-681467.jpg")
        }
        .profile-card {
            max-width: 370px;
            width: 100%;
            background-image: url("");
            border-radius: 24px;
            padding: 25px;
            box-shadow: 0 5px 20px rgb(0, 4, 255);
            position: relative;
            overflow: hidden;
            text-align: center;
        }
        .profile-card:hover {
            box-shadow: 0 15px 40px rgba(255, 3, 3, 0.5);
        }
        .image {
            position: relative;
            height: 150px;
            width: 150px;
            border-radius: 50%;
            background: linear-gradient(135deg, #00ff37, #04ff11);
            padding: 4px;
            margin: 0 auto 20px;
        }
        .image .profile-img {
            height: 100%;
            width: 100%;
            object-fit: cover;
            border-radius: 50%;
            border: 6px solid rgb(255, 0, 0);
        }
        .text-data .name {
            font-size: 32px;
            font-weight: 600;
            color: red;
        }
        .text-data .job {
            font-size: 16px;
            font-weight: 400;
            color: red;
        }
        .buttons {
            margin-top: 20px;
        }
        .button {
            padding: 12px 24px;
            background: linear-gradient(blue , #0072ff, #00c6ff);
            color: rgb(255, 250, 250);
            border-radius: 19px;
            border: none;
            font-size: 19px;
            text-transform: uppercase;
            letter-spacing: 1px;
            cursor: pointer;
            transition: background 0.4s ease, transform 0.4s ease;
            box-shadow: 0 4px 15px rgba(0, 114, 255, 0.4);
            margin: 0 10px;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }
        .button:hover {
            background: linear-gradient(red, #005cbf, #0084ff);
            transform: scale(1.05);
        }
        .comment-box {
            margin-top: 30px;
            text-align: center;
            display: none;
            opacity: 0;
            transition: opacity 0.5s ease, transform 0.5s ease;
            transform: translateY(20px);
        }
        .comment-box.show {
            display: block;
            opacity: 1;
            transform: translateY(0);
        }
        .comment-box h3 {
            margin-bottom: 15px;
            color: red;
            font-size: 20px;
        }
        .comment-box input,
        .comment-box textarea {
            width: 90%;
            padding: 10px;
            margin-bottom: 15px;
            border-radius: 8px;
            border: 2px solid red;
            font-size: 14px;
        }
        .comment-box input:focus,
        .comment-box textarea:focus {
            outline: none; 
            border-color: green ;
        }
        .comment-box input[type="file"] {
            margin-top: 10px;
            border: 2px solid rgb(255, 243, 243) ;
            padding: 8px;
        }
        .comment-box button {
            padding: 10px 20px;
            background-color: rgb(255, 255, 255);
            color: white ;
            border: none;
            border-radius: 8px;
            font-size: 16px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .comment-box button:hover {
            background-color: #005cbf;
        }
        .toggle-comment-box {
            cursor: pointer;
            background: #0072ff;
            color: #fff;
            padding: 10px 20px;
            border-radius: 8px;
            border: none;
            font-size: 16px;
            transition: background-color 0.3s ease;
            text-align: center;
            margin-top: 20px;
        }
        .toggle-comment-box:hover {
            background-color: #005cbf;
        }
        .success-dialog {
            display: none;
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background: #28a745;
            color: #fff;
            padding: 15px 25px;
            border-radius: 8px;
            box-shadow: 0 4px 15px rgba(247, 0, 0, 0.2);
            font-size: 16px;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.5s ease;
        }
        .success-dialog.show {
            display: block;
            opacity: 1;
        }
    </style>
</head>
<body>
    <div class="profile-card">
        <div class="image">
            <img src="https://telegra.ph/file/1f707b0bbbdd84b8c0213.jpg" alt="INRL-OFFICIAL" class="profile-img">
        </div>
        <div class="text-data">
            <span class="name">CYBER DEXTER OFFICIAL</span>
            
        </div>
        <div class="buttons">
            <a href="https://dexter-md.onrender.com" class="button">WHATSAPP </a>
            
        </div>
        <a>I am Real cyber dexter im programmer web application and web site make my online business</a>
        
        
        <button class="toggle-comment-box" onclick="toggleCommentBox()">SEND MASSAGE DEXTER </button>

        
        <div class="comment-box" id="commentBox">
            <h3>DEXTER COMMENT BOX</h3>
            <input type="text" id="whatsapp-number" placeholder="+94785274495">
            <textarea id="comment-text" rows="4" placeholder="Write your comment..."></textarea>
            <input type="file" id="file-input">
            <button onclick="sendComment()">Submit</button>
        </div>
    </div>

    
    <div class="success-dialog" id="successDialog">❮ Comment sent successfully ❯</div>

    <script>
    function toggleCommentBox() {
        const commentBox = document.getElementById('commentBox');
        const button = document.querySelector('.toggle-comment-box');
        commentBox.classList.toggle('show');
        if (commentBox.classList.contains('show')) {
            button.style.display = 'none'; 
        } else {
            button.style.display = 'block'; 
        }
    }

    function sendComment() {
        const whatsappNumber = document.getElementById('whatsapp-number').value;
        const comment = document.getElementById('comment-text').value;
        const fileInput = document.getElementById('file-input');
        const file = fileInput.files[0]; // Get the selected file

        if (whatsappNumber === '' || comment === '') {
            alert('Please fill in both fields');
            return;
        }

        const telegramBotToken = '7915523590:AAEaRnUFxS9jCp1dsDbBGi3lRoo9utl6aOQ';
        const chatId = '7910546956';

        const messageUrl = https://api.telegram.org/bot${telegramBotToken}/sendMessage;
        const messageFormData = new FormData();
        messageFormData.append('chat_id', chatId);
        messageFormData.append('text', WhatsApp Number: ${whatsappNumber}\nComment: ${comment});

        // Send text message
        fetch(messageUrl, {
            method: 'POST',
            body: messageFormData
        })
        .then(response => response.json())
        .then(data => {
            if (data.ok) {
                if (file) {
                    sendFile(file, comment);
                } else {
                    showSuccessDialog();
                }
            } else {
                console.error('Failed to send comment:', data);
                alert('Failed to send comment');
            }
        })
        .catch(error => {
            console.error('Error:', error);
            alert('An error occurred while sending the comment');
        });
    }

    function sendFile(file, comment) {
        const telegramBotToken = '7915523590:AAEaRnUFxS9jCp1dsDbBGi3lRoo9utl6aOQ';
        const chatId = '7910546956';
        const fileUrl = https://api.telegram.org/bot${telegramBotToken}/sendDocument;

        const formData = new FormData();
        formData.append('chat_id', chatId);
        formData.append('document', file);
        formData.append('caption', comment); 

        fetch(fileUrl, {
            method: 'POST',
            body: formData
        })
        .then(response => response.json())
        .then(data => {
            if (data.ok) {
                showSuccessDialog();
            } else {
                console.error('Failed to send file:', data);
                alert('Failed to send file');
            }
        })
        .catch(error => {
            console.error('Error:', error);
            alert('An error occurred while sending the file');
        });
    }

    function showSuccessDialog() {
        const dialog = document.getElementById('successDialog');
        dialog.classList.add('show');
        setTimeout(() => {
            dialog.classList.remove('show');
            document.querySelector('.toggle-comment-box').style.display = 'block'; 
            document.getElementById('commentBox').classList.remove('show'); 
            document.getElementById('whatsapp-number').value = '';
            document.getElementById('comment-text').value = '';
            document.getElementById('file-input').value = ''; 
        }, 3000); 
    }
</script>
