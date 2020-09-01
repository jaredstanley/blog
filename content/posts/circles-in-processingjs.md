---
title: Circles in processing.js
description: Here's the code
month: 02
day: 04
year: 2012
---
Here’s the code:


```
int numberOfPoints = 360;
float angleIncrement = 360 / numberOfPoints;
float circleRadius = 200;
Item[] items;
int count = 0;
void setup() {
background(255);
size(700, 700);
noStroke();
smooth();
items = new Item[numberOfPoints];
for(int i = 0; i
items[i] = new Item(i, 0,0);
}
}
void draw() {
background(255);
for (int i = 0; i < numberOfPoints; i++) {
items[i].update();
}
}
class Item {
int id;
float x;
float y;
float s, newS;
float r, g, b;
float radius;
float newRadius;
Item(int iid, float ix, float iy) {
s = random(15);
newColor();
radius = random(300)+50;
id = iid;
}
void update() {
setTargetPoint();
x = (newRadius * cos((angleIncrement * id) * (PI / 180 )));
y = (newRadius * sin((angleIncrement * id) * (PI / 180 )));
x += width/2;
y += height/2;
fill(r, g, b, 240);
ellipse( x, y, newRadius/5, newRadius/5);
}
void setTargetPoint() {
newRadius += (radius-newRadius)/10;
if(abs(newRadius - radius)
radius = random(300)+50;
}
}
void newColor() {
r = random(255);
g = random(100);
b = random(10);
}
}
```