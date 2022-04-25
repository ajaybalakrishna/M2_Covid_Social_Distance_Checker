# OBJECTIVE OF THIS PROJECT : 
The objective of the Covid Social distance checker is to check whether the distance between the source and destination is more than 2 meter or less than 2 meter. If the distance is less than 2 meter, it is indicated to the user via Red LED else green Led is turned on.

# INTRODUCTION :

Covid Social distance checker mainly uses ultrasonic sensor to calculate the distance between the source and obstacle is more than 2 meters or not. If the distance between them is less than 2 meters, a red LED is used to indicate that the distance is less than 2 meters. If the distance between them is more than 2 meters, a green LED will turn on. 

# PRINCIPLE:
* Ultrasonic Module HC-SR04 works on the principle of SONAR and RADAR system. 
* HC-SR-04 module has an ultrasonic transmitter, receiver, and control circuit on a single board.

# COMPONENTS AND SUPPLIES :
* ATMega328
* Ultrasonic Sensor (HC-SR04)
* Resistor
* LED's (green -1, Red -1)
* Voltage Source
* Connecting wires
* Potentiometer
* LCD display (Hd44780-84)

# working :
* ATmega328 microcontroller needs to transmit at least 10 us trigger pulse to the ultrasonic sensor Trigger Pin.
* After getting a trigger pulse, ultrasonic sensor automatically sends eight 40 kHz sound waves and the microcontroller waits for rising edge output at the Echo pin.
* When the rising edge capture occurs at the Echo pin which is connected to an input of ATmega328, start Timer of ATmega328 and again wait for a falling edge on the Echo pin.
* As soon as the falling edge is captured at the Echo pin, the microcontroller reads the count of the Timer. 
* This time count is used to calculate the distance to an object.


# Calculation  

* Sound velocity =   343.00 m/s = 34300 cm/s

* The distance of Object (in cm) = (Sound Velocity * TIMER)/2             

                               = (34300 cm/s * TIMER)/2

                               = ( 17150 * TIMER ) cm

* Now, here we have selected an internal 8 MHz oscillator frequency for ATmega328, with No-presale for timer frequency. 

* Then time to execute 1 instruction is 0.125 us.

* So, the timer gets incremented after 0.125 us time elapse.

                 = 17150 x (TIMER value) x 0.125 x 10^-6 cm

                 = 0.125 x (TIMER value)/58.30 cm

                 = (TIMER value) / 466.47 cm

# Applications  :
* This device can be employed in pandemic situations such as covid-19 where social distancing is necessary. 
* This can also be used in government offices or public places where the people waiting in queue to maintain social distancing.
* this can also be used in schools and colleges to have adequate distance between the students.
 
# Advantages and Disadvantages :
# Advantages :
* In pandemic situations like Covid-19, It is very much necessary in the workspace to maintain social distancing which gives confident to the employees that the workspace is safe.
* It is very easy to build and use.
* No many components are required.


# Disadvantages :
* It may be different for someone to carry always wherever he/she goes.
* Size may be little big to carry.


# Cost and Availability :
* Due to its basic architecture, the ultrasonic sensor is inexpensive and widely available in the market, both offline and online.  
* The following are some of the online stores where I propose you shop:
  1. ELECTRONICSCOMP
  2. THINKROBOTICS
  3. ROBU.IN \sAMAZON \sFLIPKART
