- š Hi, Iām @xolu1993
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
xolu1993/xolu1993 is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
var MAX_RADIUS = 100;
var MAX_CIRCLES = 100;
var counter = 0;

function start(){
	setTimer(draw, 50);
}

function draw(){
	drawCircle(Randomizer.nextInt(0, MAX_RADIUS),
			   Randomizer.nextColor(),
			   Randomizer.nextInt(0, getWidth()),
			   Randomizer.nextInt(0, getHeight()));
	
	counter++;
	
	if(counter == MAX_CIRCLES){
		stopTimer(draw);
	}
}

function drawCircle(radius, color, x, y){
	var circle = new Circle(radius);
	circle.setColor(color);
	circle.setPosition(x, y);
	add(circle);
}
