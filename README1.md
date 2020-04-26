# processing
컴퓨터그래픽스 수업을 할 때 필요한 것
void setup() {
  size(640, 360); //화면에 보일 크기
  background(102); //배경의 흑백 채도
}

void draw() {
  stroke(255); //하얀색 펜
  if (mousePressed == true) { //조건문이고 마우스를 누른다면 누른 좌표부터 이동한 좌표까지 이어준다
    line(mouseX, mouseY, pmouseX, pmouseY);
  }
}
