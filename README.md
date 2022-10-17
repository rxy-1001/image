# image
织布
PImage img;

void setup(){
  size(700,1000);
  background(255);
  noStroke();
  img=loadImage("image01.jpg");
}
void draw(){
  int a=int(random(0,1000));
  int b=int(random(0,700));
  int c=int(random(1,3));
  fill(0);
  rect(0,a,width,c);
  rect(b,0,c,height);
  blend(img,0,a,width,c,0,a,width,c,ADD);
  blend(img,b,0,c,height,b,0,c,height,ADD);
}
void mousePressed(){
  img=loadImage("image02.jpg");
  draw();
}
