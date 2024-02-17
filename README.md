Performance Testing of ESC
Performance testing of the E-Service Center application using Apache JMeter. Evaluate system behavior under various load conditions to ensure stability and reliability. Includes test scenarios, results analysis, and recommendations for optimizing performance.

Contents
*Introduction

*Prerequisites

*APIs Tested

*Installation

*Performance Testing Scenarios

*Results Analysis

*Result Attactments

*Html Report

*Recommendations

Introduction
This project focuses on performance testing of the E-Service Center application using Apache JMeter. Performance testing helps in evaluating the system's behavior under different load conditions to ensure its stability and reliability.

Prerequisites
Ensure that you have Apache JMeter installed on your system. If not, download and install it from

Apache JMeter website.
Download the E-Service Center project from the GitHub repository:

E-Service Center GitHub Repository
Clone or download the project and set it up in your localhost environment to perform API testing.

APIs Tested
http://localhost/E-Service-Center/index.php
http://localhost/E-Service-Center/Requester/RequesterLogin.php
http://localhost/E-Service-Center/Requester/RequesterProfile.php
http://localhost/E-Service-Center/Requester/SubmitRequest.php
http://localhost/E-Service-Center/Requester/submitrequestsuccess.php
http://localhost/E-Service-Center/logout.php
Installation
Download the provided JMX file.
Open Apache JMeter.
Open the downloaded JMX file in Apache JMeter.
Performance Testing Scenarios
Load Testing
Configure the test plan for 520 threads, ramp-up period of 10 seconds, and loop count of 1.
Run the test plan to simulate the load with 520 users.
Load Testing Variation
Modify the test plan for 540 threads.
Run the test plan to simulate the load with 540 users.
Endurance Testing
Modify the test plan for 540 threads and duration of 10 minutes.
Run the test plan to simulate the endurance test with 540 users over a 10-minute period.
Spike Testing
Modify the test plan for 700 threads.
Run the test plan to simulate the spike test with a sudden increase in load with 700 threads.
Running the Test
Click the "Run" button in Apache JMeter to start the test plan execution.
Monitor the test results for response times, error rates, throughput, and other relevant metrics.
Results Analysis
Analyze the results generated by Apache JMeter to identify performance bottlenecks, errors, and areas for improvement.
Use JMeter's built-in listeners and reporting tools to view and analyze test results.
Results Attachment All the summary reports with different amount of threads. The summary report provides a summary of the total number of requests, average response time, error count etc for the entire test plan.

520 Threads

The summary reports shows the total number of requests which is 5720 and error rate is 0 % in this scenario.

560 threads

Here the attachment shows 6160 requests and the total error rate is 0.26% and the throughput is 40.9/sec. 580 Threads

In the above scenario the number of request is 6380 and with this the error rate is above one percent which is 1.82% so the system behavior with this amount of request is not so good. 700 threads

For spike testing I have loaded the system which a huge number of threads which is 700, in this scenario system behavior degrades and the error rate is 7.31%.

Recommendations
Adjust thread counts, ramp-up periods, and loop counts based on your application's requirements and expected usage patterns.
Run multiple iterations of the tests to ensure consistency and reliability of the results.
Consider running the tests on different environments (e.g., local, staging, production) to simulate real-world conditions.
