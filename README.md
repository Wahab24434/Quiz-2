Certainly! Below is a simple HTML and JavaScript code that presents three names of Allah in Arabic, each with three pronunciation options. The user can choose the correct pronunciation, and a score will be displayed based on the number of correct answers.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Names of Allah Quiz</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
        }
    </style>
</head>
<body>
    <h1>Names of Allah Quiz</h1>

    <div id="quiz-container">
        <div id="question1" class="question">
            <p>1. اَلرَّحْمَٰنُ</p>
            <form id="form1">
                <input type="radio" name="q1" value="correct"> Al-Rahman
                <input type="radio" name="q1" value="wrong1"> Al-Rahim
                <input type="radio" name="q1" value="wrong2"> Al-Malik
            </form>
            <span id="score1"></span>
        </div>

        <div id="question2" class="question">
            <p>2. الْمَلِكُ</p>
            <form id="form2">
                <input type="radio" name="q2" value="wrong1"> Al-Aziz
                <input type="radio" name="q2" value="correct"> Al-Malik
                <input type="radio" name="q2" value="wrong2"> Al-Quddus
            </form>
            <span id="score2"></span>
        </div>

        <div id="question3" class="question">
            <p>3. الْقُدُّوسُ</p>
            <form id="form3">
                <input type="radio" name="q3" value="wrong1"> Al-Khaliq
                <input type="radio" name="q3" value="wrong2"> Al-Mu'min
                <input type="radio" name="q3" value="correct"> Al-Quddus
            </form>
            <span id="score3"></span>
        </div>

        <button onclick="calculateScore()">Submit Answers</button>
    </div>

    <script>
        function calculateScore() {
            var score1 = document.querySelector('input[name="q1"]:checked').value === 'correct' ? 1 : 0;
            var score2 = document.querySelector('input[name="q2"]:checked').value === 'correct' ? 1 : 0;
            var score3 = document.querySelector('input[name="q3"]:checked').value === 'correct' ? 1 : 0;

            document.getElementById('score1').innerText = 'Score: ' + score1;
            document.getElementById('score2').innerText = 'Score: ' + score2;
            document.getElementById('score3').innerText = 'Score: ' + score3;

            var totalScore = score1 + score2 + score3;
            alert('Your total score: ' + totalScore);
        }
    </script>
</body>
</html>
```

This code sets up a simple quiz with three questions, each related to a name of Allah. The user selects their answers, and upon clicking the "Submit Answers" button, a total score is displayed. You can customize the quiz further based on your preferences.
