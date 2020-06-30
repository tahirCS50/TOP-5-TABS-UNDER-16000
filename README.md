# TOP-5-TABS-UNDER-16000
<!DOCTYPE HTML>
<html>
<head>  
<script type="text/javascript">
window.onload = function () {

var chart = new CanvasJS.Chart("chartContainer", {
	animationEnabled: true,
	title:{
		text: "Top 5 Tabs under 16000"
	},
	axisY: {
		title: "Tablets"
	},
	legend: {
		cursor:"pointer",
		itemclick : toggleDataSeries
	},
	toolTip: {
		shared: true,
		content: toolTipFormatter
	},
	data: [{
		type: "bar",
		showInLegend: true,
		name: "Samsung Galaxy Tab A 10.1",
		color: "#8fb339",
		dataPoints: [
            { y: 61, label: "DESIGN" },
			{ y: 46, label: "DISPLAY" },
            { y: 70, label: "PERFORMANCE" },
            { y: 46, label: "CAMERAS" },
            { y: 59, label: "AUDIO" },
            { y: 52, label: "BATTERY" },
			{ y: 69, label: "PROCESSOR"},
			{ y: 88, label: "FEATURES" }
		]
	},
	{
		type: "bar",
		showInLegend: true,
		name: "Lenovo Tab M10 FHD REL  ",
		color: "#01baef",
		dataPoints: [
          { y: 59, label: "DESIGN" },
			{ y: 44, label: "DISPLAY" },
            { y: 65, label: "PERFORMANCE" },
            { y: 36, label: "CAMERAS" },
            { y: 85, label: "AUDIO" },
            { y: 52, label: "BATTERY" },
			{ y: 61, label: "PROCESSOR"},
			{ y: 84, label: "FEATURES" }
		]
	},
	{
		type: "bar",
		showInLegend: true,
		name: "iBall iTAB MovieZ Tablet",
		color: "#e8871e",
		dataPoints: [
          { y: 65, label: "DESIGN" },
			{ y: 42, label: "DISPLAY" },
            { y: 55, label: "PERFORMANCE" },
            { y: 40, label: "CAMERAS" },
            { y: 55, label: "AUDIO" },
            { y: 45, label: "BATTERY" },
			{ y: 24, label: "PROCESSOR"},
			{ y: 68, label: "FEATURES" }
         ]
    },
     {
		type: "bar",
		showInLegend: true,
		name: "HUAWEI MediaPad T5  ",
		color: "#4b5842",
		dataPoints: [
          { y: 59, label: "DESIGN" },
			{ y: 46, label: "DISPLAY" },
            { y: 77, label: "PERFORMANCE" },
            { y: 44, label: "CAMERAS" },
            { y: 59, label: "AUDIO" },
            { y: 53, label: "BATTERY" },
			{ y: 67, label: "PROCESSOR"},
			{ y: 82, label: "FEATURES" }
		]
	},
     {
		type: "bar",
		showInLegend: true,
		name: "Lenovo Yoga Tab 3 10 Tablet",
		color: "#414288",
		dataPoints: [
         { y: 67, label: "DESIGN" },
			{ y: 44, label: "DISPLAY" },
            { y: 62, label: "PERFORMANCE" },
            { y: 32, label: "CAMERAS" },
            { y: 65, label: "AUDIO" },
            { y: 57, label: "BATTERY" },
			{ y: 61, label: "PROCESSOR"},
			{ y: 67, label: "FEATURES" }
		]
	}]
});
chart.render();

function toolTipFormatter(e) {
	var str = "";
	
	var str3;
	var str2 ;
	for (var i = 0; i < e.entries.length; i++){
		var str1 = "<span style= \"color:"+e.entries[i].dataSeries.color + "\">" + e.entries[i].dataSeries.name + "</span>: <strong>"+  e.entries[i].dataPoint.y + "</strong> <br/>" ;
		
		str = str.concat(str1);
	}
	str2 = "<strong>" + e.entries[0].dataPoint.label + "</strong> <br/>";
	
	return (str2.concat(str));
}

function toggleDataSeries(e) {
	if (typeof (e.dataSeries.visible) === "undefined" || e.dataSeries.visible) {
		e.dataSeries.visible = false;
	}
	else {
		e.dataSeries.visible = true;
	}
	chart.render();
}

}
</script>
</head>
<body>
<div id="chartContainer" style="height: 900px; width: 100%;"></div>
<script src="https://canvasjs.com/assets/script/canvasjs.min.js"></script>
</body>
</html>
