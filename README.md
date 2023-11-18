# Smart_Irrigation_System
// AUTOMATIC IRRIGATION SYSTEM
/* The program for AUTOMATIC IRRIGATION SYSTEM IS Written and Tested by__
 HS Sandesh Hegde
 Harish P Nair
 HV Sampad Nayak
DISCLAIMER: This is a Open Source Software and This Software is distributed in the hope that it will be useful,             but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. 
Connection Details 
ARDUINO PINS
0_________________N/C 1_________________N/C
2_________________LCD-14 3_________________LCD-13 4_________________LCD-12
5_________________LCD-11
6_________________N/C
7_________________WATER_LEVEL_STATUS_LED
8_________________N/C
9_________________SPEAKER
10________________N/C
11________________LCD-6 12________________LCD-4
13________________PUMP_STATUS_LED)_AND_TO_RELAY
A0________________SOIL_MOISTURE_SENSOR
A4________________LM35_(TEMPERATURE_SENSOR) 
LCD-1_____________GND
LCD-5_____________GND
LCD-2_____________+Vcc
LCD-3_____________LCD_BRIGHTNESS
*/
 
#include <LiquidCrystal.h> //LCD Library
#define NOTE_C4 262 
#define NOTE_D4 294 
#define NOTE_E4 330 #define NOTE_F4 349 
#define NOTE_G4 392 #define NOTE_A4 440 #define NOTE_B4 494 #define NOTE_C5 523 
int temp; //int T_Sensor = A4; int M_Sensor = A0; int W_led = 7; int P_led = 13; int Speaker = 9; int val; int cel; LiquidCrystal lcd(12, 11, 5, 4, 3, 2);
void setup()
 {
    lcd.begin(16, 2);
    lcd.clear(); 
    pinMode(13,OUTPUT);     pinMode(7,INPUT);     pinMode(9,OUTPUT);
    Serial.begin(9600);
    /*
    val = analogRead(T_Sensor); //Read Temperature sensor value 
    
    int mv = ( val/1024.0)*5000;     cel = mv/10;
    */     lcd.setCursor(0,1);     lcd.print("THE TECHNOCRAT");
    delay(2000);     lcd.clear();     lcd.setCursor(0,0);     lcd.print("AUTOMATIC");     lcd.setCursor(0,1);     lcd.print("IRIGATION SYSTEM");
    delay(2500);     lcd.clear(); 
