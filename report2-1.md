void setup() {
  size(800, 300); //틀의 크기
  textSize(100); //글자 크기
}
int i, dir=1, v=1; //변수선언
void draw() {    //반복
  fill(200, 80, 200); //글자색깔
  background(100, 0, 150); //배경색깔
  text("Graphics", i, 170); //문자 출력하기
  if (i>width-420) dir=-1; //좌우로 왔다가 다시 갈 수 있도록
  i = i+dir*v; //키보드로 속도 조절
  if (i<0) dir=1; //
}
void keyPressed() { //키보드로 속도 조절하기 위해
  v = key - '0';
}
