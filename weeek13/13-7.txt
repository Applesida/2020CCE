void setup(){//開新的
  size(1024,400);
  textFont( createFont("標楷體", 80));
}
void draw(){
  background(#3E8DF7);//色碼
  int s = second();   //Value from 0 - 59
  int m = minute();   //Value from 0 - 59
  int h = hour();     //Value from 0 - 23
  textSize(80);
  text( h + ":" + m + ":" + s, 100, 200);
  int total = s + 60*m + 60*60*h;//現在總秒數
  int closeH=17, closeM=40, closeS=0;//下課的精確時間
  int total2=closeS + 60*closeM + 60*60*closeH;//目標總秒數
  int ans = total2 - total;
  text( "剩下幾秒:" + ans, 100, 100);
  int ansH=ans/60/60%60,  ansM=ans/60%60, ansS=ans%60;
  text(ansH  +  ":" + ansM +  ":" + ansS, 100, 300);
}   //數字  字串 數字 字串 數字