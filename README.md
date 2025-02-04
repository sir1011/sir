<!DOCTYPE html>

<html lang="en">

<head>

  <meta charset="UTF-8">

  <meta name="viewport" content="width=device-width, initial-scale=1.0">

   <title>Will you be my Valentine?</title>

  <style>

        body {

            text-align: center;

            font-family: Arial, sans-serif;

            margin-top: 50px;

        }

        button {

            font-size: 20px;

            padding: 10px 20px;

            margin: 20px;

            cursor: pointer;

            border: none;

            border-radius: 5px;

        }

        .cat {

            width: 200px;

            margin-top: 20px;

        }

        .sad-cat {

            display: none;

        }

        .happy-cat {

            display: none;

        }

        .content {

            display: none;

        }

    </style>

</head>

<body>



<h1>Enter Password to Continue</h1>

<input type="password" id="password" placeholder="Enter password" />

<button id="submit-password">Submit</button>



<div class="content">
    <h1>Will you be my Valentine?</h1>

 <button id="yes-btn">Yes</button>

  <button id="no-btn">No</button>



   <img src="https://i.imgur.com/NM1mJ7G.png" alt="Sad Cat" class="cat sad-cat" id="sad-cat">
    <img src="https://i.imgur.com/tSSuNH9.png" alt="Happy Cat" class="cat happy-cat" id="happy-cat">

</div>



<script>

    const password = '10112004sir.'; // Set the password

    const submitPasswordBtn = document.getElementById('submit-password');

    const passwordInput = document.getElementById('password');

    const contentDiv = document.querySelector('.content');

    

    const yesBtn = document.getElementById('yes-btn');

    const noBtn = document.getElementById('no-btn');

    const sadCat = document.getElementById('sad-cat');

    const happyCat = document.getElementById('happy-cat');



    submitPasswordBtn.addEventListener('click', () => {

        if (passwordInput.value === password) {

            contentDiv.style.display = 'block';  // Show the Valentine options

            passwordInput.value = ''; // Clear the password input

        } else {

            alert('Incorrect password! Please try again.');

        }

    });



    yesBtn.addEventListener('click', () => {

        sadCat.style.display = 'none';

        happyCat.style.display = 'block';

    });



    noBtn.addEventListener('click', () => {

        happyCat.style.display = 'none';

        sadCat.style.display = 'block';

    });

</script>



</body>

</html>

document.addEventListener("DOMContentLoaded", function () {
    console.log("Page 2 script loaded!");});
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Will You Be My Valentine?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #ffebee;
            color: #d32f2f;
            margin: 0;
            padding: 0;
        }
        section {
            padding: 50px;
        }
        .hidden {
            display: none;
        }
        .btn {
            background-color: #e91e63;
            color: white;
            padding: 15px 30px;
            border: none;
            cursor: pointer;
            font-size: 18px;
            border-radius: 10px;
        }
        .cat-img {
            width: 200px;
            height: auto;
        }
    </style>
</head>
<body>
    <section id="passwordSection">
        <h2>Enter the Secret Password</h2>
        <input type="password" id="passwordInput" placeholder="Enter password">
        <button class="btn" onclick="checkPassword()">Submit</button>
        <p id="errorMessage" style="color:red; display:none;">Wrong password! Try again.</p>
    </section>
    <section id="quizPassword" class="hidden">
        <h2>Enter the Second Password</h2>
        <input type="password" id="quizPasswordInput" placeholder="Enter password">
        <button class="btn" onclick="checkQuizPassword()">Submit</button>
        <p id="quizErrorMessage" style="color:red; display:none;">Wrong password! Try again.</p>
    </section>
    <section id="quiz" class="hidden">
        <h2>Answer These Questions</h2>
        <p>Select the correct answers to continue!</p>
        <div id="questions"></div>
        <button class="btn" onclick="checkAnswers()">Submit Answers</button>
    </section>
    <section id="success" class="hidden">
        <h2>Proud of you Babyy Ji! I love youuu 💖</h2>
        <img src="https://dragon.online-convert.com/download-file/7f8b6904-79f6-4372-8db7-b6b781b799c5/7b1f91c4-3159-4af3-99c4-d0fa372466be" alt="Happy Cat" class="cat-img">
        <p>I love youuu hehh 💕</p>
    </section>
    <section id="failure" class="hidden">
        <h2>Try Again!</h2>
        <img src="https://dragon.online-convert.com/download-file/fddda5fe-a5d3-4e06-bfa9-a375ad5bacdc/82cdea82-9679-49c5-a3fb-c90604ac43b1" alt="Sad Cat" class="cat-img">
        <p>Oops, wrong answer! Try again, love. 💔</p>
        <button class="btn" onclick="showSection('quiz')">Retry</button>
    </section>
    <script>
        function checkPassword() {
            const password = "10112004sir."; // Set your first password here
            const input = document.getElementById("passwordInput").value;
            if (input === password) {
                document.getElementById("passwordSection").classList.add("hidden");
                showSection("quizPassword");
            } else {
                document.getElementById("errorMessage").style.display = "block";
            }
        }
        function checkQuizPassword() {
            const quizPassword = "bhalu"; // Set your second password here
            const input = document.getElementById("quizPasswordInput").value;
            if (input === quizPassword) {
                document.getElementById("quizPassword").classList.add("hidden");
                showSection("quiz");
                generateQuestions();
            } else {
                document.getElementById("quizErrorMessage").style.display = "block";
            }
        }
        function showSection(id) {
            document.querySelectorAll('section').forEach(sec => sec.classList.add('hidden'));
            document.getElementById(id).classList.remove('hidden');
        }
        function generateQuestions() {
            const questions = [
                { q: "date of our milan?", options: ["twenty six", "twenty nine", "twenty seven", "twenty eight"], correct: "twenty nine" },
                { q: "Which food do we both love?", options: ["Pizza", "Biryani", "Ice Cream", "Pasta"], correct: "Ice Cream" },
                { q: "what i love the most?", options: ["me", "not me", "maybe me", "definetly me"], correct: "definetly me" },
                { q: "What is my favorite thing about you?", options: ["Smile", "Eyes", "Voice", "Everything"], correct: "Everything" },
                { q: "Who is genius among us?", options: ["ofc reeya", "ofc mai", "dono", "koi ni"], correct: "ofc reeya" }
            ];
            const container = document.getElementById("questions");
            container.innerHTML = "";
            questions.forEach((item, index) => {
                let optionsHTML = "";
                item.options.forEach(option => {
                    optionsHTML += `<label><input type='radio' name='q${index}' value='${option}'> ${option}</label><br>`;
                });
                container.innerHTML += `<p>${item.q}</p>${optionsHTML}<br>`;
            });
        }
        function checkAnswers() {
            const answers = ["twenty nine", "Ice Cream", "definetly me", "Everything", "ofc reeya"];
            let correct = true;
            answers.forEach((answer, index) => {
                const selected = document.querySelector(`input[name='q${index}']:checked`);
                if (!selected || selected.value !== answer) {
                    correct = false;
                }
            });
            if (correct) {
                showSection("success");
            } else {
                showSection("failure");
            }
        }
    </script>
</body>
</html>
