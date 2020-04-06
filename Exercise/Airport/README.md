# Airport


### **Deadline**
8:00AM Wednesday, April 8, 2020


### **Problem**

Assume we want to design a flight management system for Iranian airports.
We know that in each city, there are some airports and in each airport, there is an air traffic control (watchtower) that their main work is to manage flights from origin to destination.
For example, Mehrabad airport in Tehran controls all flights that their origin or destination is in this airport and for example assume that a flight from Isfahan's Shahid Beheshti airport at 11:00AM with certain number of passengers, pilots, and flight attendants is on its way to Tehran's Mehrabad Airport, and the system must store all the information related to this process.

This system will have different users such as passengers, pilots, flight attendants, guardians of the care towers, etc. which should have access to their own information.

Now you need to design an OOP (object-oriented programming) model that provides the information and capabilities required for the processes of this flight control system. 

**Note** : you just need to design and model this problem, not implement it.

**Note** : Only fields are needed to be written for each class (methods are not required) and it is necessary to use inheritance.


We wrote the Airport class and the rest is up to you :)

```
enum AirplaneType {
  Fighter, Passenger;
 }
 
public class Airplane {

 private String airplaneName;  // e.g. "777X"
 private int capacity;         // e.g. 500
 private String companyName;   // e.g. "Boeing"
 private AirplaneType type;    // e.g. AirplaneType.Passenger
}
```
