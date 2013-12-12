hackerati-assignment
====================

Assignment for Hackerati

## About ##
This assignment consists of a system that generates datapoints and stores them in a database. It also consists of a web app that can display the data at different intervals. 

## setup system ##
The system that generates/stores data is written in Java and consists of two programs: 

Collectdata.java
Stores a data value and a timestamp (epoch time) in a database. 

Gendata.java: 
generates data and passes it as arguments to Collectdata. 

### Dependencies ###
Collectdata uses two external jar libraries: 
- ini4j (http://ini4j.sourceforge.net/)
- JDBC driver for MySQL (http://dev.mysql.com/downloads/connector/j/)
When compiling Collectdata, these must be on the CLASSPATH. 

### Run system ###
Compile the system by the command 'javac Gendata.java Collectdata.java' 
The run the system by the command 'java Gendata <interval> <n>
The arguments are: 

interval: The time interval between each generated datapoint. It can be either 'minute', 'hour', or 'day'. First datapoint has the current timestamp. 
n: Number of datapoints generated. 

It is also possible to call Collectdata directly like this 'Collectdata <time> <val>'
time: Timestamp of datapoint in 'epoch' format. 
val: some integer value. 

