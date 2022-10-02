# Random-User-API-Performance-Test


## Test Scenario
Here Load testing is performed using a random API (https://random-data-api.com/api/v2/users) where the expected load is 120000 in 12 Hour. Several tests has been performed for 60s,300s,600s and 900s load using Jmeter to find out system Performance and Stability. 

## Challenges
- Does Actual TPS(Transaction Per Second) meet the expected required TPS.
- Finding out the Bottleneck/Stress test point of the system.

## Pre-requisite
1. Install jdk 8 or any LTS version
2. Download and extract Apache Jmeter 5.5 or any latest version
3. Configure JAVA_HOME and JMETER_HOME in system environment variable

## Overall TPS and Load Test Breakdown
### Load Test Strategy
![Report](https://user-images.githubusercontent.com/40294642/193454321-133b86ab-5df9-4cff-993c-8fccc4ccfdc4.png)

### Load Test Results

- Test 1. 60 sec and 167 Users/Threads
![Test_1](https://user-images.githubusercontent.com/40294642/193454423-7dd1fe08-ffd2-4a09-b48f-ca31d766aa3d.png)

- Test 2. 300 sec and 833 Users/Threads
![Test_2](https://user-images.githubusercontent.com/40294642/193454443-057e3dbb-73f7-4706-a03e-2863b86e4eb8.png)

- Test 3. 600 sec and 1667 Users/Threads
![Test_3](https://user-images.githubusercontent.com/40294642/193454480-55b615a9-4933-4828-bdb1-67f1d38152a3.png)

- Test 4. 900 sec and 2500 Users/Threads
![Test_4](https://user-images.githubusercontent.com/40294642/193454495-b3ba738e-2d6f-47ca-9801-706c5fad141a.png)

- **HTML Summary Report**
![HTML Report](https://user-images.githubusercontent.com/40294642/193454728-483762de-c452-4f3c-8a90-45a4df512da1.png)
                 
- **CLI Result Tree**
                                                                  
   ![CLI Summary](https://user-images.githubusercontent.com/40294642/193454873-2042bc47-2658-4d96-8de8-e08929f7c892.png)



## Finding out the Bottleneck/Stress test point

- Strategy to Finding out the Bottleneck/Stress test point
![Report](https://user-images.githubusercontent.com/40294642/193454944-bf3af7ac-0c54-4c18-a50c-93999283492d.png)

- The Bottleneck/Stress test point (System starts to show error with 26.3 TPS for 300 Sec, while handling 8000 user/threads)
![Bottleneck Point](https://user-images.githubusercontent.com/40294642/193454998-08860534-21d7-49ba-9b2a-a3c66628712a.png)

- **HTML Summmary Report**
![HTML Report](https://user-images.githubusercontent.com/40294642/193455080-5987f34a-c352-41fb-958d-663fdcf8dcf4.png)

- **CLI Result Tree**
                                                       
    ![Summary](https://user-images.githubusercontent.com/40294642/193455092-f1708439-10e9-4331-b371-cef4a42b05ba.png)

