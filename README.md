# Hi, I'm Gopal Girhe 👋

## Performance Testing Engineer | Pune India

### 🔧 Skills
- Apache JMeter 5.6.3
- Load Testing | Stress Testing | Spike Testing
- API Performance Testing
- CSV Parameterization & Correlation
- Non-GUI Execution & HTML Reports
- Grafana InfluxDB Monitoring
- Postman | SQL

### 📁 Projects

#### 🛫 WebTours Flight Booking -JMeter Performance Test
- End-to-end load test on flight booking application
- 6 transaction flows -Register, Login, Search, Select, Book, Signoff
- CSV parameterization with 10 unique users
- APDEX Score: 1.000 | Error Rate: 0% | 30 Samples

#### 🛒 Demoblaze E-Commerce -JMeter Performance Test
- End-to-end load test on e-commerce application
- Cookie-based authentication
- Complete shopping flow -Login, Browse, Add to Cart, Checkout

#### 🔌 ReqRes API -JMeter Performance Test
- REST API performance testing
- Bearer token authentication using JSON Extractor
- GET and POST API load testing

### 📊 Performance Testing Knowledge
- HTTP Status Codes | Bottleneck Analysis
- SLA | SLO | SLI concepts
- Monitoring with Grafana + InfluxDB
- APM Tools - New Relic, Dynatrace awareness
- JMeter Plugins - Concurrency Thread Group

### 🎯 Currently
Seeking Junior Performance Testing Engineer roles in Pune

### 📫 Contact
- Email: gopallgirhe@gmail.com

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
