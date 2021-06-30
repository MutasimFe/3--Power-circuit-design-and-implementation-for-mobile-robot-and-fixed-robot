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

If i want to make a battery that provide 12 voltage and 12Ah i have two ways to get:
   
------------------------------------------------------------------------------------------------------------------------------------------------

### 1- i will connect individual batteries to get these values

I have chosen the Li-ion battery because of Li-ion batteries are able to be recharged hundreds of times and are more stable. They tend to have a higher energy density, voltage capacity and lower self-discharge rate than other rechargeable batteries. This makes for better power efficiency as a single cell has longer charge retention than other battery types. 

But remember this type of battery is expensive which is the main disadvantage.

**But remember it's worth for all its characteristics**

In this case i will chose one of two battries **18650 - MJ1** or **18650 - 35E** 
        
![600x601](https://user-images.githubusercontent.com/85455361/123690920-a6630f00-d85d-11eb-854b-65d425171c95.png)
![8d00fe7c-053e-4744-993a-85cef1662b9f](https://user-images.githubusercontent.com/85455361/123690903-a19e5b00-d85d-11eb-97f4-15b1eeec260c.jpg)


   Each of them provides: **3.7V** and **3500mAh** for each single cell
         
   So to have 12 volt with 12Ah i will connect:
         
   following the same concept of following figure:   
         
![BatteriesWiredSeriesParallel](https://user-images.githubusercontent.com/85455361/123692468-83d1f580-d85f-11eb-8ad9-5b942d02c39a.jpg)
         
   1. Connect 4 cells in series to increase the voltage, thus will give me 4*3.7 = 14.8V
   
   2. Connect four of 14.8 voltage in parallel to have the mAh, thus we will have 4*3500= 14mAh; which is even more than required for 3 hours

![circuit (3)](https://user-images.githubusercontent.com/85455361/123959515-f0133d00-d9b6-11eb-9be0-12645d81b893.png)


   I can use **26650A battery** as well and the arrangement would not be exactly the same  
   
   
   ![image](https://user-images.githubusercontent.com/85455361/123694373-ef1cc700-d861-11eb-82b0-debee829d146.jpg)

------------------------------------------------------------------------------------------------------------------------------------------------

### 2-Using a existing battries:
This is an easier way and it will eliminate us from making a charging circuit because it will have a charger too.

------------------------------------------------------------------------------------------------------------------------------------------------

   
# (2) Charging Circuit:

## Diagram 

I designed the charging circuit ass following figure

but sadly I am not familiar with the advanced simulation platforms and the available simulation platforms are not supporting all equipment so I used the Circuit Diagram platform for drawing the electrical circuit, and when I get familiar with the advanced platform I will the connection to make sure that the circuit is working successfully. 


![circuit (2)](https://user-images.githubusercontent.com/85455361/123962467-2acaa480-d9ba-11eb-8f68-84e18a19c22c.png)

## Notes and Explanation The Diagram

note* the description would be from left to right

1. Transformer

   I used a transformer to reduce the voltage into a usable voltage.

![transformer](https://user-images.githubusercontent.com/85455361/123964352-01127d00-d9bc-11eb-8394-447e8230a0cd.png)

2. Full-Wave Recifier

   Then I used a full-wave rectifier to convert the AC voltage into DC voltage, and also it is following with 10mH inductor and 100μF for smoothing the DC voltage.

![download](https://user-images.githubusercontent.com/85455361/123964634-4c2c9000-d9bc-11eb-97d5-3f683fef7135.png)

3. LM371

  Which is the voltage regulator giving a constant dc voltage; it works by changing the resistors to have the wanter voltage.
  
![download (1)](https://user-images.githubusercontent.com/85455361/123966182-d45f6500-d9bd-11eb-9572-0948a33c0a2c.png)

  The diodes are mostly for protections
  
4. Zened diodes
   
   Zener diodes are for protection and regulate the voltage too.

    
![Zener](https://user-images.githubusercontent.com/85455361/123964508-2606f000-d9bc-11eb-84fd-19a0c91872db.gif)

# (3) Full Circuit 



# Suggest an Extra Idea/Notes:
    


