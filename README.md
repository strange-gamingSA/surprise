<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            overflow: hidden; /* Hide overflowing elements */
        }

        .container {
            text-align: center;
            position: relative;
        }

        h1 {
            color: #333;
        }

        button {
            padding: 10px 20px;
            font-size: 16px;
            margin: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #ddd;
        }
    </style>
    <title>Love Proposal</title>
</head>

<body>

    <div class="container">
        <h1>Will you be my forever love?</h1>
        <button id="yesBtn" onclick="showResponse('Yes')">Yes</button>
        <button id="noBtn" onmouseover="replaceNo(true)" onmouseout="replaceNo(false)">No</button>
    </div>

    <script>
        function showResponse(response) {
            alert("You said: " + response);
        }

        function hideNo() {
            document.getElementById("noBtn").style.display = "none";
        }

        function replaceNo(isHovered) {
            const noBtn = document.getElementById("noBtn");
            if (isHovered) {
                noBtn.innerText = "Yes";
                noBtn.onclick = function () {
                    showResponse('Yes');
                };
            } else {
                noBtn.innerText = "No";
                noBtn.onclick = hideNo;
            }
        }
    </script>
</body>

</html>
