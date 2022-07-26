<html>
<head>
    <title>Generar Urls - Doujin-Paradise</title>
<style>
    * {
        padding: 0;
        margin: 0;
        box-sizing: border-box;
    }
    body {
        background: #000;
        color: rgb(119, 119, 119);
        font-family: system-ui;
        text-align: center;
        margin-top: 5em;
    }
    input {
        margin-top: 1em;
        background: #777777;
        padding: 0.5em;
        width: 10%;
        border-radius: 0.5em;
        font-size: large;
    }
    textarea {
        background: #2a2a2a;
        color: #fff;
    }
</style>
</head>
<body>
    <h1>Generar Urls</h1>
    <form name="seccion">
        <h3>Generar urls</h3>
        <textarea name="generarurls" cols="40" rows="10"></textarea>
        <h3>Urls Generadas</h3>
        <textarea name="urlsgeneradas" cols="40" rows="10"></textarea>
        <br>
        <input type="button" value="Generar" onclick="generar()">
    </form>
    <script>
        function generar() {
            var key = document.seccion.generarurls.value;
                key = key.replace(/https/gi,'"https');
                key = key.replace(/webp/gi,'webp",');
            document.seccion.urlsgeneradas.value = key
        }
    </script>
</body>
</html>
