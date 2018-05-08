/**********************************************************************************************************

  Program Name: NodeMCU

  Decripition: This program allows user to connect wifi module NodeMCU (ESP8266) to the wifi to control any 

               electrincs device using the BLYNK Application on any smart phone or tablets from any where

               in the world.

               BLYNK ?!!!!!!!    

               Blynk is a platform with iOS and Android apps to control Arduino, Raspberry Pi and the 

               linkes over the Internet. You can easily build graphic interfaces for all your projects by

               simply dragging and dropping widgets.

               

  Programers NameS: TALHA TALLAT and BADER AL MUSKARI

  This is the link for the library that we used  https://github.com/blynkkk/blynk-library/releases/latest 

  Blynk library is licensed under MIT license

  This example code is in public domain.

  This example runs directly on NodeMCU.



  Note: This requires ESP8266 support package:

    https://github.com/esp8266/Arduino

*********************************************************************************************************/

 
#define BLYNK_PRINT Serial //This statement allows us to define a variable which print this to the serial monitor 

#include <ESP8266WiFi.h>  // we are including the libraries for the wifi module ESP8266

#include <BlynkSimpleEsp8266.h> // we are including the varible library for the wifi module 

char auth[] = "649ece09308e4ea28276c3c3a1f2dc90"; /* This is a Auth Token code that we got from by logging in to our BLYNK app account 

and setting up a ESP8266 device to the BlYNK. Another words, this is how we are connecting our phone to that wifi module. */

char ssid[] = "Arduino-Network"; // This is for ssid for our wifi to connect to the network  

char pass[] = "arduino2016"; // And obviously the security password for connecting to the chosen network

void setup()  // In setup everything runs only ones 

{

  Serial.begin(9600); //The serial monitor is used for shown the information provided and bot rate is det onto 9600

  Blynk.begin(auth, ssid, pass); // When the Token, ssid and password is valid then its start showing that wifi is cconnected on the serial Monitor 

}

void loop() //Everthing in the loop function runs continuosly 

{

  Blynk.run(); //The blynk application runs over again and again 

}

