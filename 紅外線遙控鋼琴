#include<IRremote.h>
int IRPin = A0;
int Buzzer = 13;

//tone
int so = 196;
int la = 220;
int si = 247;
int Do = 262;
int Re = 294;
int Mi = 330;
int Fa = 349;
int So = 392;
int La = 440;
int Si = 494;
int Doo = 524;

int a = 250;//1/4
int b = 500;//1/2
int c = 1000;//1
int d = 1500;//1.5
int e = 62;//1/16
int z = 750;//3/4
int s = 3000;//3

IRrecv IR(IRPin);
decode_results results;

void setup() {
  Serial.begin(9600);
  IR.enableIRIn();
  pinMode(Buzzer,OUTPUT);
}

void loop() {

  if(IR.decode(&results)){
    Serial.println(results.value,HEX);
    if(results.value==0xFFA25D){
      tone(Buzzer,Do,300);
      delay(1000);
    }
    if(results.value==0xFF629D){
      tone(Buzzer,Re,300);
      delay(1000);
    }
    if(results.value==0xFFE21D){
      tone(Buzzer,Mi,300);
      delay(1000);
    }
    if(results.value==0xFF22DD){
      tone(Buzzer,Fa,300);
      delay(1000);
    }
    if(results.value==0xFF02FD){
      tone(Buzzer,So,300);
      delay(1000);
    }
    if(results.value==0xFFC23D){
      tone(Buzzer,La,300);
      delay(1000);
    }
    if(results.value==0xFFE01F){
      tone(Buzzer,Si,300);
      delay(1000);
    }
    if(results.value==0xFFA857){
      tone(Buzzer,Doo,300);
      delay(1000);
    }
    if(results.value==0xFF38C7){
      //主旋律
        //6
        tone(Buzzer,Do,b);delay(b);
        delay(20);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        //7
        tone(Buzzer,La,z);delay(z);
        delay(20);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,Si,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        //8
        tone(Buzzer,Re,c);delay(c);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,la,a);delay(a);
        tone(Buzzer,so,a);delay(a);
        tone(Buzzer,la,c);delay(c);
        delay(b);
        tone(Buzzer,so,b);delay(b);
        //9
        tone(Buzzer,Do,c);delay(c);
        delay(20);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,la,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        delay(20);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,Re,c);delay(c);
        delay(b);
        tone(Buzzer,so,a);delay(a);
        tone(Buzzer,la,a);delay(a);
        //10
        tone(Buzzer,Do,b);delay(b);
        delay(20);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        //11
        tone(Buzzer,La,z);delay(z);
        delay(20);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,Si,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        //12
        tone(Buzzer,Re,c);delay(c);
        delay(10);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,la,a);delay(a);
        tone(Buzzer,so,a);delay(a);
        tone(Buzzer,la,c);delay(c);
        delay(b);
        tone(Buzzer,Do,b);delay(b);
        //13
        tone(Buzzer,si,z);delay(z);//3/4
        tone(Buzzer,Do,e);delay(e);//1/16
        tone(Buzzer,si,e);delay(e);//1/16
        tone(Buzzer,la,b);delay(b);
        tone(Buzzer,so,b);delay(b);
        tone(Buzzer,la,c);delay(c);
        delay(50);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,b);delay(b);
      
        //14
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,La,b);delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        //15
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,Si,b);delay(b);
        delay(20);
        tone(Buzzer,Si,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        delay(10);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,La,c);delay(c);
        delay(20);
        tone(Buzzer,La,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        //16
        tone(Buzzer,La,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        //17
        tone(Buzzer,Re,z);delay(z);//3/4
        tone(Buzzer,Mi,e);delay(e);//1/16
        tone(Buzzer,Re,e);delay(e);//1/16
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,b);delay(b);
        tone(Buzzer,Mi,c);delay(c);
        delay(20);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,b);delay(b);
        
        
        //18
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,La,b);delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        //19
        tone(Buzzer,Mi,b);delay(b);
        tone(Buzzer,Si,b);delay(b);
        delay(20);
        tone(Buzzer,Si,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        delay(10);
        tone(Buzzer,So,b);delay(b);
        tone(Buzzer,La,c);delay(c);
        delay(20);
        tone(Buzzer,La,b);delay(b);
        tone(Buzzer,So,b);delay(b);
        //20
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,La,c);delay(c);
        tone(Buzzer,So,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,Doo,c);delay(c);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        //21
        tone(Buzzer,So,s);delay(s);//3
        delay(b);
        tone(Buzzer,so,a);delay(a);
        tone(Buzzer,la,a);delay(a);
      
      
        //22
        //10
        tone(Buzzer,Do,b);delay(b);
        delay(20);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Do,b);delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Mi,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        //11
        tone(Buzzer,La,c);delay(c);
        delay(10);
        tone(Buzzer,La,a);delay(a);
        delay(10);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,Si,a);delay(a);
        tone(Buzzer,La,a);delay(a);
        tone(Buzzer,So,a);delay(a);
        tone(Buzzer,Mi,c);delay(c);
        delay(b);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Mi,a);delay(a);
        //12
        tone(Buzzer,Re,c);delay(c);
        tone(Buzzer,Re,a);delay(a);
        tone(Buzzer,Do,a);delay(a);
        tone(Buzzer,la,a);delay(a);
        tone(Buzzer,so,a);delay(a);
        tone(Buzzer,la,c);delay(c);
        delay(b);
        tone(Buzzer,Do,b);delay(b);
        //13
        tone(Buzzer,si,z);delay(z);//3/4
        tone(Buzzer,Do,e);delay(e);//1/16
        tone(Buzzer,si,e);delay(e);//1/16
        tone(Buzzer,la,b);delay(b);
        tone(Buzzer,so,b);delay(b);
        tone(Buzzer,la,c);delay(c);
        delay(c);
    }
    
    IR.resume();
  }
}
