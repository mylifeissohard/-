int motorLF = 5, motorLB = 6, motorRF = 9, motorRB = 10;
int TrigL = A2, EchoL = A3,TrigR = A5, EchoR = A4; 
int IRL = A0; int IRR = A1; 
int IRRState;  int IRLState;
float echotimeL, distanceL, echotimeR, distanceR;
float T = 22.0, v = (331+0.6*T) * 100/1000000 ;
void setup() {
  Serial.begin(9600);  
  pinMode(motorLF, OUTPUT); pinMode(motorLB, OUTPUT); 
  pinMode(motorRF, OUTPUT); pinMode(motorRB, OUTPUT); 
  pinMode(TrigL, OUTPUT);  pinMode(EchoL, INPUT); 
  pinMode(TrigR, OUTPUT);  pinMode(EchoR, INPUT); 
    pinMode(IRL, INPUT);  pinMode(IRR, INPUT); 
  Serial.println(v);  
 }

void Distance_L() {
digitalWrite(TrigL, HIGH); delay(5);    
digitalWrite(TrigL, LOW);  
echotimeL = pulseIn(EchoL, HIGH);
distanceL = v*(echotimeL/2);  }

void Distance_R() {
digitalWrite(TrigR, HIGH); delay(5); digitalWrite(TrigR, LOW); 
echotimeR = pulseIn(EchoR, HIGH); distanceR = v*(echotimeR/2);   }

 void Forward() {
   analogWrite(motorLF, 0);//左往後
   analogWrite(motorLB, 75);//左往前 
   analogWrite(motorRF, 0);//右往後
   analogWrite(motorRB, 80); }//右往前
   
 void Back() {
   analogWrite(motorLF, 60);//左往後
   analogWrite(motorLB, 0);//左往前 
   analogWrite(motorRF, 65);//右往後
   analogWrite(motorRB, 0); }//右往前

void turnLeft() {//右轉
   analogWrite(motorLF, 0);
   analogWrite(motorLB, 60);    
   analogWrite(motorRF, 0);
   analogWrite(motorRB, 0); }

void turnRight() {//左轉
   analogWrite(motorLF, 0);
   analogWrite(motorLB, 0);    
   analogWrite(motorRF, 0);
   analogWrite(motorRB, 55); }


void Stop() {
   analogWrite(motorLF, 0);
   analogWrite(motorLB, 0);    
   analogWrite(motorRF, 0);
   analogWrite(motorRB, 0); }

 
void loop() {  
   IRLState = digitalRead(IRL);   IRRState = digitalRead(IRR);
   Distance_L();   
   Distance_R();   // DistanceL_R(); 
   if (distanceL <= 15 and distanceR <= 15) { Stop(); }
   if (distanceL > 15 and distanceR > 15) { 
    if (IRLState == 0  and IRRState ==  0){ Forward(); }//走黑線，1==>白
    if (IRLState ==  1 and IRRState ==  0 ){ turnRight(); }//右邊白==>左轉
    if (IRLState ==  0 and IRRState ==  1 ){ turnLeft(); }//左邊白==>右轉
    if (IRLState ==  1 and IRRState ==  1 ){ Stop(); }   }//兩邊黑==>停 }
   if (distanceL < 15 or distanceR < 15) { 
        if (distanceR > distanceL) {  Stop();/*Back();delay(300);*/turnLeft();delay(300); } 
        if (distanceR < distanceL) {  Stop();/*ㄝBack();delay(300);*/turnRight();delay(300);}  
        }
   Serial.print(" L =  ") ;  Serial.print(distanceL); 
   Serial.print(" ; R =  "); Serial.println(distanceR);
   }
