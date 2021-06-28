# 3-Power circuit design and implementation for mobile robot and fixed robot

# The Main Idea Of This Task: 

This task is devided into 3 sub-tasks which are related to each other. 


In this task I:


1. I choose which battery is the best battery for the fighter robot.

2. Since the chosen battery must be a rechargeable battery, I made the electrical circuit of charging the chosen battery.

3. Last I connected the circuit of the previous task ( 2 dc motors ) with the charging circuit. 



# (1) Chosing Battery:

## Components of the circuit: 

In this section i will define the operating voltages/currents of all components that is using in the Fighter Robot. 

1. Arduino:

        The operating voltage: 5v (most common) or 3.3V

        The operating current: 20mA per I/O port
        
        The totale current of all pins: 200mA 
       
2. DC Motors x4: 

    Dc motors are not specified by a specific type so I will take the average operation current at 6-12 voltages.
    
        The operating voltage: 6-12V 

        The operating current: 300mA-1.2A
        
        The total current consumption: i will take the average (1200-300)/2 * 4 = 1800mA = 1.8A
       
       

3. L298N Dual H-Bridgle x2:

        The operating voltage: 5-35voltage but 5 voltage will be considered in our robot

        The operating current: 36mA
        
        The totale current consumption:  36mA*2 = 72mA

4. Servo Motors x5:

        The operating voltage: 4.2-7V usually at 6V

        The operating current: 350-450mA 
        
        The totale current consumption: i will consider the avergae current which is 400*5 = 2000mA = 2A

## Maximum Voltage and Total Current: 

So, the total current of all components are: 
 
        200mA + 1.8A + 72mA + 2A = 4072 mA which approximately equal to 4A

*Note that: this total current is upon my assumption which means it can be larger or smaller but approximately around it.

The maximum voltage used is:

        12v

## Life Time: 

   The life time of the battery is basically can be calculated using this follow farmula:

        Time = Total Battery Supply (mAH) / Total Current Consumption (mA) ; the total current is known above and the time is set by the developer 
        
   So, since the project is a fighter robot which means the life time of batter doesnt have to be so long and in my openioin 3 hours are enough
   
   Thus, the Total Battery Supply (mAH) must be:
   
        Total Battery Supply(mAH) = 3hours * 4000mA = 12000 mAh

## Main Constraints Of Chosing Battery: 

From above we know that the two main constraints that must be conderated in chosing the battery are:

1. The maximum voltage is: 12V

2. Total Battery Supply(mAH) = 12000mAh

## The Chosen Battery:

   If i want to make a battery that provide 12 voltage and 12Ah i have t2o ways to get:
   
   1. i will connect individual batteries to get these values


   2. Using a existing battries:



   
   
   
# (2) Charging Circuit:



# (3) Full Circuit 



# Suggest an Extra Idea/Notes:
    


