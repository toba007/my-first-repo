function setup() {
  let posX = 40; 
  let posY = 150;

  createCanvas(250, 180); 
  background(255);        
  noStroke();             

  fill(0); 
  textSize(36); 
  textStyle(BOLD); 
  text('accenture', posX, posY); 

  // 「＞」の描画 ---
  fill(161, 0, 255); 

  // posX を基準に計算しているため、文字に合わせて左へ
  let markX = posX + 95; 
  let markY = posY - 50; 

  // ＞の形を quad で再現
  //quad(左上, 左下, 右下, 右上) の順で座標を指定
  // ① ＞の上半分（右下へ向かう四角形）
  quad(markX, markY, markX, markY + 6, markX + 20, markY + 14, markX + 20, markY + 8);
  // ② ＞の下半分（左下へ向かう四角形）
  quad(markX + 20, markY + 8, markX + 20, markY + 14, markX, markY + 22, markX, markY + 16);

  //  補助線
  stroke(220); 
  line(posX, posY + 15, posX + 200, posY + 15);
}
