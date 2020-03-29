void setup(){
  size(800,300); //틀의 크기
  textSize(100); //글자 크기
}
int i, j=1; //변수선언
void draw(){    //반복
  fill(200,80,200); //글자색깔
  background(100,0,150); //배경색깔
  if(keyPressed) //키보드를 누르는 값을 숫자로 표현하기위해
   j = key-'0'; //숫자 변환
  text("andong", i=i+j, 170); //문자 출력하기
  if(i>800) i=0; //좌우 800길이에서 다시 돌아가게 할려고
}
