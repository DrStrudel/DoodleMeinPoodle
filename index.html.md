<!doctype html>
<html lang="en-US">
    <head>
        <meta charset="utf-8"/>
        <title>Länktest</title>
        <style>
            h1{
            color: <?php
                echo $_GET["color"];
            ?>;
            }
        </style>
    </head>
    <body>
        <?php
            if(isset($_GET["namn"])){
                $namn=htmlspecialchars($_GET["namn"],ENT_QUOTES, "UTF-8");
                echo "<h1> Hej ", $namn, "</h1>";
            }
            else{
                 
        ?>
        <form action="" method="GET">
            Namn: <input type="text" name="namn"><br />
            Färg: <input type="text" name="color"><br>
            <input type="submit" value="Send">
        </form>
        <?php } ?>
    </body>
</html>
