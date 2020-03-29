PFont f;
void setup(){
  size(800,400);
  textSize(100);
  f = createFont("굴림", 64);
  textFont(f);
}
int i, v=1;
void draw(){
  background(30,0,30);
  fill(255,0,255);
  text("안동대 컴공 사랑합니다", 40, i);
  if(i>400) i = 0;
  i = i+v;
}
void keyPressed(){
  v = key-'0';
}
