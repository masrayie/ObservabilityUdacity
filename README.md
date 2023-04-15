**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation
*TODO:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

### Monitoring Namespace
<img width="1014" alt="Screen Shot 2023-04-14 at 23 29 50" src="https://user-images.githubusercontent.com/38803630/232178260-d3f456c5-fadd-4949-868a-2835459acc54.png">

### Observability Namespace
<img width="1161" alt="Screen Shot 2023-04-14 at 23 30 14" src="https://user-images.githubusercontent.com/38803630/232178268-a693c561-b379-4722-85f5-0612618bbefa.png">

### ProjectApp
<img width="983" alt="Screen Shot 2023-04-15 at 09 58 51" src="https://user-images.githubusercontent.com/38803630/232179842-865072f2-3794-4260-ad3c-1f0f43714cb1.png">

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.
<img width="1678" alt="Screen Shot 2023-04-14 at 23 31 02" src="https://user-images.githubusercontent.com/38803630/232178416-16a78cbd-be9a-4152-acfe-9ba1a9e9808f.png">

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
![Screen Shot 2023-04-15 at 10 02 27](https://user-images.githubusercontent.com/38803630/232179930-8a507fdc-5efe-4ee5-be67-3f574d45310a.png)


## Describe SLO/SLI
We are trying to define our SLOs for *monthly uptime* and *request response time*:
1. 99.95% Uptime or Service Availability in the year.
2. 95% of requests completed in < 120 ms.

Then we could describe the SLIs are:
1. We achieve the availability of the app in this year is around 99.94%
2. In average, 94% of the requests were successfully completed in < 120ms

## Creating SLI metrics.
1. **Uptime Percentage:** This is a metric that measure the percentage of time that a service is available during a certain of time. For example, if a service is available for 99.9% of the month, that means it experienced 43.2 minutes of downtime during the month.

2. **Error Rate:** This metric measures the total number of errors or failures that occur during a certain of time, usually expressed as a percentage of requests. A high error rate could as indicator of issues appear due to the application code, infrastructure, or other factors.

3. **Average Response Time:** This metric can help us to monitor latency of the application and also can help to do tuning to improve the application performance.

4. **Mean Time to Repair (MTTR):** This metric measures the time it takes to resolve or fix an issue once it has been detected. A high MTTR can lead to longer periods of downtime or poor performance.

5. **Average Percentage of Resources (Memory/CPU):** This metric can help us to measure the impact of deployment services to monitor the utilization and do preventation before reach heap.

## Create a Dashboard to measure our SLIs
![Screen Shot 2023-04-15 at 10 39 10](https://user-images.githubusercontent.com/38803630/232181194-20c19692-1259-4ab4-9d4e-a9ed9b0a7ad3.png)

## Tracing our Flask App
<img width="744" alt="Screen Shot 2023-04-15 at 11 01 13" src="https://user-images.githubusercontent.com/38803630/232181932-fb0b91fc-246f-475f-b6b4-05c3c32c41d4.png">

<img width="1674" alt="Screen Shot 2023-04-14 at 23 28 17" src="https://user-images.githubusercontent.com/38803630/232178522-ac2ef52b-b702-489f-b0b6-71444f8f60f2.png">

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.

<img width="798" alt="Screen Shot 2023-04-15 at 08 40 31" src="https://user-images.githubusercontent.com/38803630/232178513-26cb6323-a96f-43c4-91ae-be3e83020e52.png">

## Report Error

**TROUBLE TICKET**

**Name:** Error on Backend URL endpoint "/star"

**Date:** 15th April 2023, 09:36:49

**Subject:** Method "GET" not Allowed for accessing the URL.

**Affected Area:** Backend App endpoint "/star"

**Severity:** ***High***

**Description:** Hitting backend url path "/star" with GET request produce error and return 405 status code. It might be caused by "GET" Method is not allowed to perform in this URL.

<img width="1677" alt="Screen Shot 2023-04-15 at 09 36 49" src="https://user-images.githubusercontent.com/38803630/232179271-a594966b-bf9e-409f-a694-57e742609614.png">

## Creating SLIs and SLOs
**SLIs:**
1. Achieve success response >75% than errors.
2. Maximum average response time is around 2000ms per minute, smaller is better.
3. Error response appearance is less than 10 errors within last 24h.
4. 99% responses from applications are serving valid data format.

**SLOs:**
1. 99.99% transaction request success for each month.
2. 99.9% backend services succeed on their first attempt.
3. 99.9% uptime services for each month.
4. 99.9% frontend services responses return all kind of HTTP Code with in 2000ms. 

## Building KPIs for our plan
- 75% or greater successful responses than errors:
1. Successfull requests in minute: this KPI will indicates the number of successful requests.
2. Error requests in minute: this KPI will indicates the number of error requests.

- Average Response Time less than 2000ms per minute.
1. Uptime: this KPI will help user to determine if the response time is impacted by downtime or anomaly of a service.
2. Average Response Time: this KPI is showing average response time of services.

- Maximum Error Response appearance is 10 within last 24h:
1. Uptime: this KPI indicates if errors are probably comming from downtime or not.
2. Successful request per minute: this KPI indicates our systems is running well or not.
3. Error requests per minute: it show any error requests coming.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
![Screen Shot 2023-04-15 at 10 08 31](https://user-images.githubusercontent.com/38803630/232180090-3f90611a-9899-4b1d-bafd-4df8b48cbc0f.png)


