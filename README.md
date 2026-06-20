# WebTours-Performance-Testing
# WebTours Flight Booking -JMeter Performance Test

## About This Project
End-to-end performance test project on Webtours-
a flight booking web application running on localhost.
Bult as part of my performance testing learning roadmap
.

## Application Under Test
  Application : Webtour (HP Demo Application)
  URL: localhost:1080
  Type :flight booking web application


## Business Scenarios Tested
- User Registration
- User Login
- Flight Search
- Flight Selection
- Payment and Booking
- Sign Off

## JMeter Components Used
| Component | Purpose |
|---|---|
| Thread Group | 5 virtual users, 10 sec ramp-up |
| HTTP Cookie Manager | Session handling |
| CSV Data Set Config | 10 unique user credentials |
| Regular Expression Extractor | Correlation for dynamic session |
| Transaction Controllers | Grouped each business flow |
| Response Assertion | Validated login and booking response |
| Duration Assertion | SLA -fails if response exceeds 5 seconds |
| Constant Timer | Think time between requests |
| Aggregate Report | 90th percentile statistics |

## Test Execution — 3 Phase Approach
Phase 1 -Debug Run: 1 user to verify script works
Phase 2 - Smoke Test: 5 users to confirm no errors
Phase 3 - Load Test: Non-GUI mode with HTML report

## Non-GUI Command Used
jmeter -n -t WebTours_Performance_Test.jmx -l results.jtl -e -o report

## Test Results Summary
- Total Samples: 30
- Error Rate: 0.00%
- Average Response Time: 102ms
- 90th Percentile: 126ms
- APDEX Score: 1.000 (Perfect)
- Throughput: 22.95 transactions/sec

## Tools Used
- Apache JMeter 5.6.3
- Java JDK 21

## Key Concepts Demonstrated
 Recording with HTTP(S) Test Scipt Recorder
 Correlation using Regular Expression Extractor
 CSV Parameterization for multiple users
 Non-GUI Execution
 HTML Report Generation
 Response and Duration Assertion
 Complete user journey from Registration to Sign Off
