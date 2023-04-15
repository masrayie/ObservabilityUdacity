**Note:** For the screenshots, you can store all of your answer images in the `answer-img` directory.

## Verify the monitoring installation
*TODO:* run `kubectl` command to show the running pods and services for all components. Take a screenshot of the output and include it here to verify the installation

### Monitoring Namespace
<img width="1014" alt="Screen Shot 2023-04-14 at 23 29 50" src="https://user-images.githubusercontent.com/38803630/232178260-d3f456c5-fadd-4949-868a-2835459acc54.png">

### Observability Namespace
<img width="1161" alt="Screen Shot 2023-04-14 at 23 30 14" src="https://user-images.githubusercontent.com/38803630/232178268-a693c561-b379-4722-85f5-0612618bbefa.png">

### ProjectApp
<img width="1025" alt="Screen Shot 2023-04-14 at 23 29 37" src="https://user-images.githubusercontent.com/38803630/232178271-56ccf3a9-af1d-4939-88d6-4e4c11a22324.png">

## Setup the Jaeger and Prometheus source
*TODO:* Expose Grafana to the internet and then setup Prometheus as a data source. Provide a screenshot of the home page after logging into Grafana.
<img width="1678" alt="Screen Shot 2023-04-14 at 23 31 02" src="https://user-images.githubusercontent.com/38803630/232178416-16a78cbd-be9a-4152-acfe-9ba1a9e9808f.png">

## Create a Basic Dashboard
*TODO:* Create a dashboard in Grafana that shows Prometheus as a source. Take a screenshot and include it here.
<img width="1680" alt="Screen Shot 2023-04-15 at 09 16 26" src="https://user-images.githubusercontent.com/38803630/232178421-491d73e2-cb0c-41a5-90d8-1b6e57622657.png">

## Describe SLO/SLI
*TODO:* Describe, in your own words, what the SLIs are, based on an SLO of *monthly uptime* and *request response time*.

## Creating SLI metrics.
*TODO:* It is important to know why we want to measure certain metrics for our customer. Describe in detail 5 metrics to measure these SLIs. 

## Create a Dashboard to measure our SLIs
*TODO:* Create a dashboard to measure the uptime of the frontend and backend services We will also want to measure to measure 40x and 50x errors. Create a dashboard that show these values over a 24 hour period and take a screenshot.

## Tracing our Flask App
*TODO:*  We will create a Jaeger span to measure the processes on the backend. Once you fill in the span, provide a screenshot of it here. Also provide a (screenshot) sample Python file containing a trace and span code used to perform Jaeger traces on the backend service.
<img width="1674" alt="Screen Shot 2023-04-14 at 23 28 17" src="https://user-images.githubusercontent.com/38803630/232178522-ac2ef52b-b702-489f-b0b6-71444f8f60f2.png">

## Jaeger in Dashboards
*TODO:* Now that the trace is running, let's add the metric to our current Grafana dashboard. Once this is completed, provide a screenshot of it here.
<img width="798" alt="Screen Shot 2023-04-15 at 08 40 31" src="https://user-images.githubusercontent.com/38803630/232178513-26cb6323-a96f-43c4-91ae-be3e83020e52.png">

## Report Error
*TODO:* Using the template below, write a trouble ticket for the developers, to explain the errors that you are seeing (400, 500, latency) and to let them know the file that is causing the issue also include a screenshot of the tracer span to demonstrate how we can user a tracer to locate errors easily.

TROUBLE TICKET

Name: Error on Backend URL endpoint "/star"

Date: 15th April 2023, 09:36:49

Subject: Method "GET" not Allowed for accessing the URL.

Affected Area: Backend App endpoint "/star"

Severity: High

Description: Hitting backend url path "/star" with GET request produce error and return 405 status code. It might be caused by "GET" Method is not allowed to perform in this URL.

<img width="1677" alt="Screen Shot 2023-04-15 at 09 36 49" src="https://user-images.githubusercontent.com/38803630/232179271-a594966b-bf9e-409f-a694-57e742609614.png">

## Creating SLIs and SLOs
*TODO:* We want to create an SLO guaranteeing that our application has a 99.95% uptime per month. Name four SLIs that you would use to measure the success of this SLO.

## Building KPIs for our plan
*TODO*: Now that we have our SLIs and SLOs, create a list of 2-3 KPIs to accurately measure these metrics as well as a description of why those KPIs were chosen. We will make a dashboard for this, but first write them down here.

## Final Dashboard
*TODO*: Create a Dashboard containing graphs that capture all the metrics of your KPIs and adequately representing your SLIs and SLOs. Include a screenshot of the dashboard here, and write a text description of what graphs are represented in the dashboard.  
<img width="1680" alt="Screen Shot 2023-04-15 at 09 25 07" src="https://user-images.githubusercontent.com/38803630/232179038-24cd1c63-0ddc-44c3-be75-7c69430a2f92.png">

