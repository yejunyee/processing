# processing
컴퓨터그래픽스 수업을 할 때 필요한 것
  
PFont f; //원하는 글씨체를 쓰기 위해
  
void setup() {
  size(640, 360);
  
  // Create the font
  printArray(PFont.list());
  f = createFont("SourceCodePro-Regular.ttf", 24);
  textFont(f); //글씨체 연결
}

void draw() {
  background(102);
  textAlign(RIGHT);
  drawType(width * 0.25); //가로의 4분의 1
  textAlign(CENTER);
  drawType(width * 0.5);
  textAlign(LEFT);
  drawType(width * 0.75);
}

void drawType(float x) {
  line(x, 0, x, 65);
  line(x, 220, x, height);
  fill(0); //색상
  text("ichi", x, 95); //쓸 글씨와 위치
  fill(51);
  text("ni", x, 130);
  fill(204);
  text("san", x, 165);
  fill(255);
  text("shi", x, 210);
}
