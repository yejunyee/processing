# processing
컴퓨터그래픽스 수업을 할 때 필요한 것

PShape bot; //bot이라는 모형 선언

void setup() {
  size(640, 360);
  
  bot = loadShape("bot1.svg"); //괄호 안에 있는 것을 불러들임
} 

void draw() {
  background(102);
  translate(width/2, height/2); //중간으로 이동
  float zoom = map(mouseX, 0, width, 0.1, 4.5); //가로의 움직임으로 인해 확대
  scale(zoom); //
  shape(bot, -140, -140);
}
