processing_start
================

ball_bounce_blinking

PVector location;
PVector velocity;

void setup() {
  size(200,200);
  location = new PVector(100,100);
  velocity = new PVector(1.5,2);
}

void draw() {
  background(random(255),random(255),random(255));
  
  location.add(velocity);
  if ((location.x > width) || (location.x < 0)) {
    velocity.x = velocity.x * -1;
  }
  if ((location.y > height) || (location.y < 0)) {
    velocity.y = velocity.y * -1;
  }
  
  stroke(0);
  fill(120);
  ellipse(location.x,location.y,10,10);
}
