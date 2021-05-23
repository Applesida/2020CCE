void setup(){//開新的
  size(1024,400);
}|
void draw(){
  background(#3E8DF7);//色碼
  int s = second();   //Value from 0 - 59
  int m = minute();   //Value from 0 - 59
  int h = hour();     //Value from 0 - 23
  textSize(80);
  text( h + ":" + m + ":" + s, 100, 200);
}   //數字  字串 數字 字串 數字