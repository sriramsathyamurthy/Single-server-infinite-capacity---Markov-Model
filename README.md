# Single server with infinite capacity (M/M/1):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 12 seconds, serivice time of lathe machine follows exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)



## Experiment:


 
## Program
```
#Developed by: SRIRAM S
#Reg No: 212225240155

arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print(f"The mean arrival rate per second : {lam:.2f}")
print(f"The mean service rate per second : {mu:.2f}")
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print(f"Average number of objects in the system : {Ls:.2f}")
    print(f"Average number of objects in the conveyor :  {Lq:.2f}")
    print(f"Average waiting time of an object in the system : {Ws:.2f} secs")
    print(f"Average waiting time of an object in the conveyor : {Wq:.2f} secs")
    print(f"Probability that the system is busy : {(lam/mu):.2f}" )
    print(f"Probability that the system is empty : {(1-lam/mu):.2f}" )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```

## Output :
```
Enter the mean inter arrival time of objects from Feeder (in secs): 20
Enter the mean  inter service time of Lathe Machine (in secs) :  3
Enter the Additional time taken for the Robot (in secs) :  4
--------------------------------------------------------------
Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)
--------------------------------------------------------------
The mean arrival rate per second : 0.05
The mean service rate per second : 0.14
Average number of objects in the system : 0.54
Average number of objects in the conveyor :  0.19
Average waiting time of an object in the system : 10.77 secs
Average waiting time of an object in the conveyor : 3.77 secs
Probability that the system is busy : 0.35
Probability that the system is empty : 0.65
---------------------------------------------------------------
```
## Result :
The average number of material in the system and in the conveyor and waiting time are succcessfully found.
