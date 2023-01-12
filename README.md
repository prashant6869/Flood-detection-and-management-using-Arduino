# Flood-detection-and-management-using-Arduino
 
Project circuit diagram : {refer this (link) circuit diagram for connections}

(https://user-images.githubusercontent.com/99020701/212123257-ad2f3fb3-e8cb-4e6c-955e-7395e5292b0a.jpg)


Methodology :

Dams are built all around the world primarily for irrigation, power generating, and flood control. While the first two tasks are acknowledged, dams' involvement in flood management has generally been underestimated. Unfortunately, flood control is entirely ignored in both irrigation and hydroelectric projects. Authorities always aim to save as much water as possible in reservoirs during the monsoon season, which is then used for irrigation and energy generating throughout the summer months. It is a globally known practise to keep a reservoir's water level below a specified level before the start of the monsoon season. This is done so that when the monsoon rains arrive, there is enough space to retain the excess rainfall and so that water may be released in a controlled manner, preventing flooding downstream when the dams are overflowing.
Overflowing dam could result in major destruction of the dam and flood in villages near the bank of the river which means major threats to human life and wildlife.
Today most of dams in India uses manual ways of detecting water level. They use water level marking on the dam’s walls to major the level of water in dam. This manual way leads to human errors and some time to major destruction.
To handle this destruction, we have implemented this on a dam model. Here we are trying to automate dams so that dams can detect water level and automatically release excess water that could leads to dam’s overflow. 
One of the main reasons of human death due to floods is because of the late alert to peoples living on the banks of the river in which dam is constructed. To overcome this, we have used GSM module which will send alert SMS to them to evacuate the area.
We have use following sensors to evaluate the current water level and situation of the dam.

-	Arduino uno 
-	Ultrasonic sensor (to measure water level)
-	Servo motor (to operate dam gate)
-	LM-35 Temperature sensor (to measure temperature)
-	Moisture sensor (to measure soil water holding capacity)
-	Float sensor (to measure blue line)
-	GSM module (to send alert SMS)

Here we have used ultrasonic sensor which will measure the water level using ultrasound. We have attached the sensor 25 cm above the base of dam. Getting the readings of the sensor to serial monitor of the Arduino IDE. We have set the condition that when the level of the dam gets above 95 percentage of total capacity then the gate of dam gets open and releases excess water up to certain level. Continues measurement are taken. 
Servo motor is used to control the operation of the gate that allow the outlet of excess water from dam. This gate operates as above explained. 
There is one container representing river in which float sensor is used. Whenever the river water level reaches blue line (maximum level of water level after which it leads to flood situations in surrounding area). 
To alert peoples about this we have buzzers and SMS system which will be trigger when float sensor hits high level. For SMS feature we have used GSM module which can send SMS to mobile phones. We need to have a dedicated sim card for SMS facility. 
Measure problem in flood control system is to include all the factors which leads to flood conditions.
Some of the factors which we have implemented are using temperature sensor and moisture sensor. Here we calculate water holding capacity of soil by moisture sensor and calculating evaporation rate using temperature sensor. This both factors are which are ignored or not considered. 
We have also considered tomorrow’s rain fall as a major factor for flood control. We are using this to predict how much rain will fall tomorrow and how much will the dam full after rainfall. For this we are using machine learning for predicting. 
For example, we came to know that tomorrow X amount of rain will fall and by which Y level of dam will get filled. If Y level of the dam is its upper most level above which dam will overflow.
So, to avoid this situation of overflow we remove tomorrows predicted level of water today only in control manner which should not lead to flood like situation.
Here we provide manual predicted value of rainfall as input to serial monitor of Arduino IDE. By this value ultrasonic sensor adjust its maximum and minimum level accordingly and opens gates if needed.
However, even if the prediction fails and dams fall short of water and there is a shortfall in electricity generation, this is not a loss compared to the possible loss of lives in the event of a flood of this magnitude.
We have connected all modules/sensors mention above to Arduino UNO microcontroller.


