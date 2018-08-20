<?php
$i=1;
$active_menu=array();
$now_page="";
$bmi=0;
?>
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta http-equiv="X-UA-Compatible" content="IE=edge">
		<meta name="viewport" content="width=device-width, initial-scale=1">
		<!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
		<title>โปรแกรมคำนวนค่าดัชนีมวลกาย (BMI)</title>
		<!-- Bootstrap -->
		<link href="css/bootstrap.min.css" rel="stylesheet">
		<link href="css/theme.css" rel="stylesheet">
		<!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
		<!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
		<!--[if lt IE 9]>
		<script src="https://oss.maxcdn.com/html5shiv/3.7.3/html5shiv.min.js"></script>
		<script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
		<![endif]-->
		<link rel="shortcut icon" href="images/logo.png" type="image/x-icon">
	</head>
	<body>
		<nav class="navbar navbar-khrutik navbar-static-top">
			<div class="container-fluid">
				<div class="navbar-header"><a class="navbar-brand">คำนวนค่าดัชนีมวลกาย (BMI)</a>
				<button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar">
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				<span class="icon-bar"></span>
				</button>
			</div>
			<div class="collapse navbar-collapse" id="myNavbar">
				<ul class="nav navbar-nav">
					<li class="<?php echo $active_menu[1];?>"><a href="index.php"><span class="glyphicon glyphicon-home"></span> หน้าแรก</a></li>
					<li class="<?php echo $active_menu[2];?>"><a href="index.php"><span class="glyphicon glyphicon-pencil"></span> อาหาร</a></li>
				</ul>
			</div>
			
		</div>
	</nav>
	<div class="container-fluid">
		<form class="form-horizontal" id="calbmi" name="calbmi" method="GET" action="">
			<fieldset>
				<!-- Text input-->
				<div class="form-group">
					<label class="col-md-4 control-label" for="weight">น้ำหนัก</label>
					<div class="col-md-4">
						<input id="weight" name="weight" type="text" placeholder="กิโลกรัม" class="form-control input-md">
					</div>
				</div>
				<!-- Text input-->
				<div class="form-group">
					<label class="col-md-4 control-label" for="height">ส่วนสูง</label>
					<div class="col-md-4">
						<input id="height" name="height" type="text" placeholder="เซนติเมตร" class="form-control input-md">
					</div>
				</div>
				<!-- Button -->
				<div class="form-group">
					<label class="col-md-4 control-label" for="submit"></label>
					<div class="col-md-4">
						<button id="submit" name="submit" class="btn btn-danger">คำนวนค่าดัชนีมวลกาย (BMI)</button>
					</div>
				</div>
			</fieldset>
		</form>
	</div>
	<?php
	if (empty($_GET["height"]) || empty($_GET["weight"])) {
	?>
	<p>
		<div class="container-fluid">
			<div class="panel panel-danger">
				<div class="panel-heading">
					<h3 class="panel-title">What’s BMI?</h3>
				</div>
				<div class="panel-body">
					BMI compares your weight to your height, and is calculated by dividing your weight in kilograms by your height in metres squared. It gives you an idea of whether you’re underweight, a healthy weight, overweight, or obese for your height. BMI is one type of tool to help health professionals to assess risk for chronic disease. Another important tool is waist circumference. It is also important to understand your other risk factors.
				</div>
				<div class="panel-heading">
					<h3 class="panel-title">Calculate your BMI</h3>
				</div>
				<div class="panel-body">
					BMI is a useful measurement for most people over 18 years old. But it is only an estimate and it doesn’t take into account gender, age, ethnicity and body composition. We recommend you also check your waist measurement, and other risk factors.
					
					Speak to your doctor, an Accredited Practising Dietitian or a health practitioner about your weight.
					This calculator shouldn’t be used for pregnant women or children.
				</div>
			</div>
		</div>
	</p>
	<?php
	}
	else
	{
	//$gender=$_GET["gender"];
	$height=$_GET["height"]/100;
	$weight=$_GET["weight"];
	$bmi=$weight/($height*$height);
	?>
	<p>
		<div class="container-fluid">
			<div class="panel panel-danger">
				<div class="panel-heading">
					<h3 class="panel-title">ค่าดัชนีมวลกาย (BMI) = <?php echo number_format($bmi, 2, '.', '');?></h3>
				</div>
				<?php
				if($bmi<16)
				{
				?>
				<div class="panel-body">
					โรคผอม ระดับ 3
				</div>
				<?php
				}
				else if($bmi<17)
				{
				?>
				<div class="panel-body">
					โรคผอม ระดับ 2
				</div>
				<?php
				}
				else if($bmi<18.5)
				{
				?>
				<div class="panel-body">
					โรคผอม ระดับ 1
				</div>
				<?php
				}
				else if($bmi<23)
				{
				?>
				<div class="panel-body">
					ปกติ
				</div>
				<?php
				}
				else if($bmi<25)
				{
				?>
				<div class="panel-body">
					น้ำหนักเกิน
				</div>
				<?php
				}
				else if($bmi<30)
				{
				?>
				<div class="panel-body">
					โรคอ้วน ระดับ 1a
				</div>
				<?php
				}
				else if($bmi<35)
				{
				?>
				<div class="panel-body">
					โรคอ้วน ระดับ 1b
				</div>
				<?php
				}
				else if($bmi<40)
				{
				?>
				<div class="panel-body">
					โรคอ้วน ระดับ 2
				</div>
				<?php
				}
				else
				{
				?>
				<div class="panel-body">
					โรคอ้วน ระดับ 3
				</div>
				<?php
				}
				?>
			</div>
		</div>
	</p>
	<?php
	}
	?>
</div>
<div class="container-fluid">
	*** สำหรับประเมินภาวะโภชนาการในผู้ที่มีอายุตั้งแต่ 18 ปีขึ้นไป
	<p> </p>
</div>
<!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js"></script>
<!-- Include all compiled plugins (below), or include individual files as needed -->
<script src="js/bootstrap.min.js"></script>
</body>
</html>
