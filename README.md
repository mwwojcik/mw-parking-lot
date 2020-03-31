
## Table of contents
- [Design of Computer System supporting large area Parking Lot](#design-of-computer-system-supporting-large-area-parking-lot)
  - [Table of contents](#table-of-contents)
  - [Intro](#intro)
  - [Domain description](#domain-description)
## Intro
This is a design of computer system supporting large scale parking lot. It was implemented for educational purposes using techniques derived from the domain of DDD.

![](img/parking-lot-small.png)

Imagine that you, and your team was asked for designing comprehensive computer system for parking lots.
This project was commissioned by the company "Stay Not Pay", which manages a network of dynamically growing car parks. 
This company has invested heavily in developing an IT system, because existing systems are not 
very competitive and should be replaced by more modern ones.


Enjoy!

## Domain description
A single parking lot consists of several levels (usually from 3 to 5). On each of them can be parked 500 cars.
Parking log has many entry and exit gates.  The customer must get an entry ticket at each entrance gate. 
This ticket is the basis for calculating the amount due, which must be paid when customer is leaving out  by 
the exit gate. The amount due may be paid in three ways:

    * at the automated cash register (during leaving out)
    * at the customer’s info portal mounted on each parkig level (in this case, he doesn’t have to pay at the exit)
    * directly to the parking lot employee (then leaving out is free)

 Parking payment system should handle both cash and credit card payments.
 
 System should control the number of cars entering the parking lot. When the last parking space is occupied, system
 should be able to show a message at the paarking display board on the level 0, and close all entrance gates.

The car park has various types of places: compact, large, handicapped for different types of vehicles: car, truck, van, motorcycle. 
The system should should be able to charge different fees for each of them, and showing any free parking spot for each spot type.
 
Panel lot has a spots dedicated for electric cars. It offers charging service. System should be able to register start 
and stop of charging, and calculate the amount due.

The system should support a per-hour parking fee model. 
For example, customers have to pay $4 for the first hour, $3.5 for the second and third hours, and $2.5 for all the remaining hours.

## Domain exploration
### Big Picture Event Storming  

![](img/process-modeling-events.png)