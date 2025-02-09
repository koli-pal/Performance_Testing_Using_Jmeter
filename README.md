# Performance_Testing_Using_Jmeter

This document explains how to run a performance test with JMeter for the given testing site, also includes the report for it.

# Testing Site
Testing Site - "https://restful-booker.herokuapp.com"

# Technologies Used
- Jmeter
  

  

## Prerequisites
- **Apache JMeter**
- **Java 8+** (JMeter requires Java)
- **Git** for version control

# Installations
Java

https://www.oracle.com/java/technologies/downloads/
JMeter

https://jmeter.apache.org/download_jmeter.cgi
Click =>Binaries
=>apache-jmeter-5.6.3.zip

# Elements of a minimal test plan
- Thread Group The root element of every test plan. Simulates the (concurrent) users and then run all requests. Each thread simulates a single user.

- HTTP Request Default (Configuration Element)

- HTTP Request (Sampler)

- Summary Report (Listener)

# Test Plan
Testplan > Add > Threads (Users) > Thread Group (this might vary dependent on the jMeter version you are using)

- Name: Users

- Number of Threads (users): 1 to 10

- Ramp-Up Period (in seconds): 10

- Loop Count: 1

i. The **Test Plan** defines the overall configuration for test execution, including whether Thread Groups will execute concurrently or sequentially.  

ii. The **HTTP Request Defaults** component specifies default settings for all HTTP Requests, such as the server's IP address, port number, and content encoding.  

iii. Each **Thread Group** controls how HTTP Requests are executed. The number of threads represents the simulated concurrent users, while the loop count determines how many times each user will repeat the actions.  

iv. The **HTTP Header Manager** is the first element within Thread Groups, enabling the configuration of request headers that will be applied to subsequent HTTP Requests.

# Test execution (from the Terminal)
- keep your jmx file in bin
- JMeter should be initialized in non-GUI mode.
- Make a report folder in the bin folder.
- Run Command in ./jmeter folder
# Command
Jtl file generate command
```
jmeter -n -t demo.jmx -l report\demo.jtl


```
Report Generate command
```
jmeter -g report\ demo.jtl -o report\demo.html
```
# JMeter Project Images

![Image](https://github.com/user-attachments/assets/1c7003b0-16d3-4392-8d59-45c03d93cfb6)

# Report

![Image](https://github.com/user-attachments/assets/0fcbf502-e0d1-4048-acb8-c5e697c5283c)

![Image](https://github.com/user-attachments/assets/f044a1fc-dcc2-4038-9998-0041e4b4154d)

![Image](https://github.com/user-attachments/assets/1fffdd65-3ced-4bd6-a3f9-c1ef16578392)

![Image](https://github.com/user-attachments/assets/46b5cb7d-1105-4221-a470-98d429e237d0)





