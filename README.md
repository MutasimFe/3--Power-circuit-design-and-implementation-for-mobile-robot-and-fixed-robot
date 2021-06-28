# 3-Power circuit design and implementation for mobile robot and fixed robot

## The Main Idea Of This Task: 

This task is devided into 3 sub-tasks which are related to each other. 


In this task I:


1. I choose which battery is the best battery for the fighter robot.

2. Since the chosen battery must be a rechargeable battery, I made the electrical circuit of charging the chosen battery.

3. Last I connected the circuit of the previous task ( 2 dc motors ) with the charging circuit. 

## (1) Chosing Battery:

### Components of the circuit: 

In this section i will define the operating voltages/currents of all components that is using in the Fighter Robot. 

1. Arduino:

        The operating voltage: 5v (most common) or 3.3V

        The operating current: 20mA per I/O port
        
        The totale current of all pins: 200mA 
       
2. RS390 DC Motors x4: 

        The operating voltage: 6-12V which mean normally 7.5V

        The operating current: 1.34A at max efficiency 
        
        The stale current : 7.65A
        
        The totale current consumption: the 1.34A will be considered so 1.34A * 4 = 5.36A

3. L298N Dual H-Bridgle x2:

        The operating voltage: 5-35voltage but 5 voltage will be considered in our robot

        The operating current: 36mA
        
        The totale current consumption:  36mA*2 = 72mA

4. Servo Motors x5:

        The operating voltage: 4.2-7V usually at 6V

        The operating current: 350-450mA 
        
        The totale current consumption: i will consider the maximum current which is 450*5 = 2250mA = 2.25A

So, the total current of all components are: 
 
         200mA + 7.65A + 72mA + 2.25A = 10.172A
         
*Note that: this total current is upon my assumption which means it can be larger or smaller but approximately around it.

The maximum voltage used is:

        12v

## (2) Charging Circuit:

## (3) Full Circuit 



## Suggest an Extra Idea/Notes:
    


