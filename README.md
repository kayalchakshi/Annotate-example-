# Annotate-example-



http://ulflander.github.io/compendium-js/?text=Do%20you%20love%20me.%20but%20do%20you%20hate%20me%3F



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <style>
        /* .div{
            padding: 50px 10px 30px 30px;
        } */
    </style>
</head>
<body>
    <textarea id="text" height="50px" min-width="100%"></textarea>
    <br/>
    <button onclick="execute()">Submit</button>
    <script>
        function  execute(){
            var x = document.getElementById("text").value;
            console.log(x);
            var a = x.split(".");
            var split_var, split_word;
            for(var i =0; i < a.length-1; i++)
            {
                console.log(a[i]);
                split_var = a[i];
                split_var = split_var.trim();
                var sen = document.createElement("div");
                split_word = split_var.split(" ");
                console.log(split_word);
                var sentence ="";
                for(var j = 0; j < split_word.length-1; j++)
                {
                    var div = document.createElement("div");
                    div.className = "div";
                    var raw = document.createElement("div");
                    raw.className = "raw";
                    var pos = document.createElement("div");
                    pos.className = "pos";
                    pos.innerText = "noun";
                    sentence += split_word[j] + " ";
                    raw.innerHTML = sentence + "<hr/>";
                    // pos.innerHTML = "NN";
                    raw.style.padding = "30px 10px 10px 30px";
                    raw.style.textDecoration = "underline";
                    pos.style.padding = "30px 10px 10px 30px";
                    div.appendChild(raw);
                    div.appendChild(pos);
                }
                // sen.innerHTML= "<hr/>";
                sen.appendChild(div);

                document.body.appendChild(sen);

            }
        }
    </script>
</body>
</html>
