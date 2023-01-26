#COMPUTER GRAPHICS LAB 1

Daniela Quimis         254617   danielaamaray.quimis01@estudiant.upf.edu
Claudia Guallarte   



#3.1 DDA LINES 
        
In order to draw the lines, we use the functions seen in the slides and also our previous knowledgment seen in class of vectors.So our function sets with a loop(for) a pixel for our defined vector. 

void Image::DrawLineDDA(int x0, int y0, int x1, int y1, const Color& c){
	float dx = x0 - x1;
	float dy = y0 - y1;
	float d = std::max(abs(dx), abs(dy));
	Vector2 v(dx / d, dy / d);
	for (int i = 0; i < d; i++) {
		SetPixelSafe(x0, y0, c);
		x0 += v.x;
		y0 += v.y;
