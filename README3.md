# processing
컴퓨터그래픽스 수업을 할 때 필요한 것
float yoff = 0.0; //실수형 변수 설정

void setup() {
  size(640, 360); //크기 설정
}
void draw() {
  background(120,30,120); //배경을 보라색으로 변경
  fill(random(0,255)); //물결모양은 흰색으로 표현
  beginShape(); //다각형을 그리기 위해 필요한 함수
  float xoff = 0;  //실수형 변수 설정     
  for (float x = 0; x <= width; x += 10) { //for문으로 반복
    
    float y = map(noise(xoff, yoff), 0, 1, 100, 200); //noise 함수로 랜덤의 변수를 생성하고 자연스럽게 서로 연결해준다
    //map함수는 noise를 매핑할려고 현재 범위의 최대 최소를 정하고 매핑하고자 하는 값을 정한다.
    vertex(x, y); //다각형을 그리기 위한 함수
    xoff += 0.5;
  }
  yoff += 0.01;
  vertex(width, height); //가로와 높이
  vertex(0, height); //가로는 0이고 높이는 존재
  endShape(CLOSE); /*vertex 함수 사용할 때 같이 쓰여지는 것이며
  ()안에 CLOSE를 써주면 vertex의 처음과 끝을 서로 연결해준다*/
  
}
