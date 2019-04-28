function setup() {
   createCanvas(800, 800);
}
var rain = [];
var bucket_height = 400;
var bucket_x=0;
var bucket_y=600;
var bucket_full = 0;
var isPressed = false;
var sum = 0;
var G = 4
function draw() {
  background(100);
  //draw the wooden pool
  fill(255,0,0);
  rect(0,500,200,3);
  //draw the rain
  fill(255)
  sum++;
  for(i=0;i<rain.length;i++){
	 rain_v = rain[i];
	 x = rain_v[0];
	 y = rain_v[1];
	 y+=8;
	 //Delete rain when it falls on a wooden pole or bucket or on the ground
	 if(y>800||(x<200&&y>500)||y>bucket_y&&x>bucket_x&&x<bucket_x+160){
		rain.splice(i,1);
	 }else{
		 rain[i] = [x,y];
		 noStroke();
		 ellipse(x,y,2,10);
	 }
  }
  for(i=0;i<2;i++){
	  init_left=Math.floor(Math.random() * 800);
	  rain.push([init_left,0]);
  }
  //draw the bucket
  drawBucket();
}
function drawBucket(){
	if(isPressed){
		bucket_x = mouseX-80;
	}
	if(bucket_full>=100){
		bucket_full=100;
	}
	fill(47,33,28);
	quad(bucket_x,bucket_y,bucket_x+50,bucket_y+100,bucket_x+110,bucket_y+100,bucket_x+160,bucket_y);
}   
function mousePressed(){ 
   isPressed=true; 
} 
function mouseReleased(){ 
   isPressed=false; 
} 
