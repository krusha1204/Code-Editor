# Code-Editor
Hello Everyone, I am happy to share my task "Code Editor" provided by "Code Alpha". Thank you team Code Alpha.
<!DOCTYPE html>

<html lang="en">

<head>

    <meta charset="UTF-8">

    <meta http-equiv="X-UA-Compatible" content="IE=edge">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <link rel="stylesheet" href="style2.css">

    <title>Code Editor</title>

    <script src="https://kit.fontawesome.com/c4254e24a8.js" crossorigin="anonymous"></script>

</head>

<body>

    <div class="container">

        <div class="left" >

            <label for="" ><i class="fa-brands fa-html5"></i>HTML</label>

            <textarea name="" id="html-code" cols="30" rows="10" onkeyup="run()"></textarea>

            <label for=""><i class="fa-brands fa-css3-alt"></i>CSS</label>

            <textarea name="" id="css-code" cols="30" rows="10" onkeyup="run()"></textarea>

            <label for=""><i class="fa-brands fa-js"></i>JavaScript</label>

            <textarea name="" id="js-code" cols="30" rows="10" onkeyup="run()"></textarea>

        </div>

        <div class="right">

            <label for=""><i class="fa-solid fa-play"></i>Output</label>

            <iframe src="" id="output" frameborder="0"></iframe>

        </div>

    </div>

    <script>

        function run(){

            let htmlcode = document.getElementById("html-code").value;

            let csscode = document.getElementById("css-code").value;

            let jscode = document.getElementById("js-code").value;

            let output = document.getElementById("output");

            output.contentDocument.body.innerHTML = htmlcode + "<style>" + csscode + "</style>";

            output.contentWindow.eval(jscode);

        }

    </script>

</body>

</html>
