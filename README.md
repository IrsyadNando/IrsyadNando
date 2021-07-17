<!DOCTYPE html>
<html>
<head>

<style type="text/css">
	
	body{
		text-align:center;
		font-family:"Roboto",sans-serif;
	}
	
	#startStopBtn{
		display:inline-block;
		margin:0 auto;
		color:#6060AA;
		background-color:rgba(0,0,0,0);
		border:0.15em solid #6060FF;
		border-radius:0.3em;
		transition:all 0.3s;
		box-sizing:border-box;
		width:8em; height:3em;
		line-height:2.7em;
		cursor:pointer;
		box-shadow: 0 0 0 rgba(0,0,0,0.1), inset 0 0 0 rgba(0,0,0,0.1);
	}
	
	#startStopBtn:hover{
		box-shadow: 0 0 2em rgba(0,0,0,0.1), inset 0 0 1em rgba(0,0,0,0.1);
	}
	
	#startStopBtn:before{
		content:"Start";
	}
	
	
	#test{
		margin-top:2em;
		margin-bottom:12em;
	}
	div.testArea{
		display:inline-block;
		width:16em;
		height:12.5em;
		position:relative;
		box-sizing:border-box;
	}
	div.testArea2{
		display:inline-block;
		width:14em;
		height:7em;
		position:relative;
		box-sizing:border-box;
		text-align:center;
	}
	div.testArea div.testName{
		position:absolute;
		top:0.1em; left:0;
		width:100%;
		font-size:1.4em;
		z-index:9;
	}
	div.testArea2 div.testName{
        display:block;
        text-align:center;
        font-size:1.4em;
	}
	div.testArea div.meterText{
		position:absolute;
		bottom:1.55em; left:0;
		width:100%;
		font-size:2.5em;
		z-index:9;
	}
	div.testArea2 div.meterText{
        display:inline-block;
        font-size:2.5em;
	}
	div.meterText:empty:before{
		content:"0.00";
	}
	div.testArea div.unit{
		position:absolute;
		bottom:2em; left:0;
		width:100%;
		z-index:9;
	}
	div.testArea2 div.unit{
		display:inline-block;
	}
	div.testArea canvas{
		position:absolute;
		top:0; left:0; width:100%; height:100%;
		z-index:1;
	}
	div.testGroup{
		display:block;
        margin: 0 auto;
	}
	
	
</style>

	<title>SpeedTest</title>
</head>
<body>


<h1>SpeedTest</h1>

	<div id="startStopBtn" onclick="startStop()"></div><br/>
	
	<div id="test">
		<div class="testGroup">
			<div class="testArea2">
				<div class="testName">Ping</div>
				<div id="pingText" class="meterText" style="color:#AA6060"></div>
				<div class="unit">ms</div>
			</div>
			<div class="testArea2">
				<div class="testName">Jitter</div>
				<div id="jitText" class="meterText" style="color:#AA6060"></div>
				<div class="unit">ms</div>
			</div>
		</div>
		<div class="testGroup">
			<div class="testArea">
				<div class="testName">Download</div>
				<canvas id="dlMeter" class="meter"></canvas>
				<div id="dlText" class="meterText"></div>
				<div class="unit">Mbps</div>
			</div>
			<div class="testArea">
				<div class="testName">Upload</div>
				<canvas id="ulMeter" class="meter"></canvas>
				<div id="ulText" class="meterText"></div>
				<div class="unit">Mbps</div>
			</div>
		
	
</body>
</html>
