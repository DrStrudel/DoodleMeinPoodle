	<!-- HTML mall -->
<!doctype html>
<html lang="en">
	<head>
		<meta charset="utf-8"/>
		<title>PHP tester</title>
<?php
//PHP kontroller
	function comp($txt){
		$ar = explode(" ", $txt);
		if($ar[1] == "+"){
			$svar = $ar[0] + $ar[2];
		
			return (int)$ar[0] + (int)$ar[2];
			}if($ar[1] == "-"){
			$svar = $ar[0] - $ar[2];
		
			return (int)$ar[0] - (int)$ar[2];
			}if($ar[1] == "*"){
			$svar = $ar[0] * $ar[2];
		
			return (int)$ar[0] * (int)$ar[2];
			}if($ar[1] == "/"){
			$svar = $ar[0] / $ar[2];
		
			return (int)$ar[0] / (int)$ar[2];
			}
		}
		$svar = "";
	if(isset($_GET["test"])){
		$txt = $_GET["test"];
		$svar=comp($txt);
		}
	
	?>
	</head>
	<body>
		<h2> Mata in dina värden </h2>
		<form action="" method="GET">
			Text: <input type="text" name="test"><br />
			<input type="submit" value="Send">
		</form>
		<h2><?php echo $svar; ?></h2>
	</body>
</html>
