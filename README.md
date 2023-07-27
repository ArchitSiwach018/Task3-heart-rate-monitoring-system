Heart rate, body temperature and blood pressure monitoring are very important parameters of human body. Doctors use various kind of medical apparatus like thermometer for checking fever or body temperature, BP monitor for blood pressure measurement and heart rate monitor for heart rate measurement. In this project, we have built an Arduino based heartbeat monitor which counts the number of heartbeats in a minute. Here we have used a heartbeat sensor module which senses the heartbeat upon putting a finger on the sensor.

Components
1. Arduino
2. Heart Beat sensor module
3. 16x2 LCD
4. Push button
5. Bread board
6. Power
7. Connecting wires

Working of Heartbeat Monitor Project...

Working of this project is quite easy but a little calculation for calculating heart rate is required. There are several methods for calculating heart rate, but here we have read only five pulses. Then we have calculated total heart beat in a minute by applying the below formula:

     Five_pusle_time=time2-time1;

      Single_pulse_time= Five_pusle_time /5;

      rate=60000/ Single_pulse_time;

where time1 is first pulse counter value

time2 is list pulse counter value

rate is final heart rate.

When first pulse comes, we start counter by using timer counter function in arduino that is millis();. And take first pulse counter value form millis();. Then we wait for five pulses. After getting five pulses we again take counter value in time2 and then we substarct time1 from time2 to take original time taken by five pulses. And then divide this time by 5 times for getting single pulse time. Now we have time for single pulse and we can easily find the pulse in one minute, deviding 600000 ms by single pulse time.Rate= 600000/single pulse time.
