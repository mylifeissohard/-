#include <WiFi.h>
#include <WiFiAP.h>
#include <WiFiClient.h>
#include <WiFiGeneric.h>
#include <WiFiMulti.h>
#include <WiFiScan.h>
#include <WiFiServer.h>
#include <WiFiSTA.h>
#include <WiFiType.h>
#include <WiFiUdp.h>
#include <HTTPClient.h>
#include <DHT.h>


//DHTesp dht;
DHT dhtROOM(36,DHT11); 

HTTPClient http;

const char* ssid = "";
const char* password = "";

double echotime; double distance; float T = 22.0; 
double v = 0.03478;
//(331+0.6*T)*(100/1000000) ;  

void setup(){
  Serial.begin(115200);
  WiFi.mode(WIFI_STA);
  WiFi.begin(ssid,password);
  Serial.print("正在連接WIFI");
  while(WiFi.status()!=WL_CONNECTED){
    Serial.print('.');
    delay(1000);
  }
  Serial.println(WiFi.localIP());
  Serial.print("RRSI:");
  Serial.println(WiFi.RSSI());//wifi強度
  Serial.println("WiFi Connected");

  dhtROOM.begin();
//   dht.setup(36, DHTesp::AM2302);
   
  pinMode(34,INPUT);//麥克風
  pinMode(35,INPUT);//超音波echo
  pinMode(36,INPUT);//溫溼度
  pinMode(4,OUTPUT);//超音波輸出trig
}

void loop() {
    //加入http message header
  http.begin("https://notify-api.line.me/api/notify");
  
  http.addHeader("Content-Type","application/x-www-form-urlencoded");
  http.addHeader("Authorization","Bearer RHYF6uYLZN5tF1tpJiC0KSGiGWN6QKbjokFm1RmILAx");
  //http.POST("message=測試");

  
//麥克風
  if(digitalRead(34)==1){
    http.POST("message=寶寶發出聲音");
  }

//溫濕度
/*
  float H = dhtROOM.readHumidity();
  Serial.print(H);
  Serial.println(" %");
  float T = dhtROOM.readTemperature();

  if(isnan(H)or isnan(T)){
    Serial.println("Failed!");
    return;
  }
  Serial.print("Humidity= ");
  Serial.print(H);
  Serial.print("  Temperature= ");
  Serial.print(T);
  Serial.println("*C");*/
  /*TempAndHumidity data = dht.getTempAndHumidity();

    if (dht.getStatus() != 0) {
        Serial.println("DHT sensor error status: " + String(dht.getStatusString()));
    
    } else if (isnan(data.humidity) || isnan(data.temperature)) {
        Serial.println("Data is NaN!");

    } else {
        Serial.print("Humidity: ");
        Serial.print(data.humidity);
        Serial.print("%  Temperature: ");
        Serial.println(data.temperature);
    }

  if(data.humidity >84){
    http.POST("message=寶寶要換尿布了");
  }*/

  
 //超音波
  digitalWrite(4, HIGH);  delay(5);  digitalWrite(4, LOW);
  echotime = pulseIn(35, HIGH);  Serial.print("echotime= ");Serial.println(echotime);
  distance = v*(echotime/2) ; 
  Serial.print("distance= ");
  Serial.print(distance);
  Serial.println(" cm");
  if (distance < 4 or distance > 400){ return; } 
  if(distance<20&&distance>4){
    http.POST("message=寶寶站起來了");
    delay(400);
  }


  String reply = http.getString();
  Serial.println(reply);
  delay(2000);
  
}
