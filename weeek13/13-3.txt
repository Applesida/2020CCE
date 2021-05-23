void setup(){//只做一次的設定
  size(1024, 400);
}
void draw(){//互動版本,每秒畫60次
  if( mousePressed ) background(255, 0, 255);//按下去時 紫色
  else background( 52, 141, 247 );//否則 淡藍色
  text(a, 512, 200);//畫出文字
}//目標: 能畫圖, mouse 按下去/移動的時候,要畫點東西/做點東西
int a=0;
void mousePressed(){
   a++; 
}