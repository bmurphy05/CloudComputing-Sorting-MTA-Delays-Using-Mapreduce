# CloudComputing-Sorting-MTA-Delays-Using-Mapreduce
Sorting MTA train delays using Map/Reduce
Goal/Description: 
	The goal for this project is to utilize python to create a script that accesses the MTA API to gather train id, timestamp, service delay, effect, and station of delay for each subway line and write the data in a csv file. Then using java to read the data of the file, I will pass the data to our Hadoop MapReduce functions to count the instance of delays for each train in order to figure out which trains run the smoothest among all of the subway tracks in New York City. Ideally if I have time we will also use the data I collected to find out which subway stops are most like to have a delay and what type of delay are more common to occur at that station.
Framework for MAP/REDUCE
Input: 
All Trains: 1-7, A-W 
All Delay Types: Construction, Maintenance, Police Activity, Medical Emergency, Accident, Demonstration, Holiday, Weather, Strike, Technical Problem, “Other.”
Effect of Delay: No service, Reduced Service, Significant Delays, Detour, Additional Service, Modified Service, Stop Moved, “Other.”
Stations: Stations affected by delays.
Time Stamp: All data, time-stamped.

1-27 = Node Number (I.E. Each train type is handled by a different computer/core, there are 27 different trains.)

Splitting: Each train type mapped separately.
1-27: Train Type - Every Delay type - Assign each Specific delay with a unique Identifier
1-27: Train Type - Station of Delay
1-27: Train Type - Effect of Delay

Mapping: 
Timing: Use Delay Identifier to sort data (hourly).
Shuffling:
Combine data from each train type(27 different trains).
Reduce:
1-27:Combine and count all delays per train, per station per hour of the day





