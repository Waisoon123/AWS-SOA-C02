# Introduction to CloudWatch

AWS CloudWatch is a **monitoring solution** for your AWS resources. It monitors your AWS resources and the applications you run on AWS in real time. You can use CloudWatch to collect and track metrics, which are variables you can measure for your resources and applications.

With CloudWatch, you gain system-wide visibility into resource utilization, application performance, and operational health.

CloudWatch is an **umbrella service**, meaning that it is a collection of monitoring tools as follows:

> [!NOTE]
> Not everything below are within the scope of the exam. The focused segments are as follows: **Logs, Metrics, Events, Alarms, Dashboards**

### Logs

We can use AWS CloudWatch Logs to monitor, store and access our log files from AWS Elastic Compute Cloud (EC2) instances, AWS CloudTrail, Route 53, and other sources. Essentially this enables us to centralize the logs from all of our systems, applications, and AWS services that we use, in a single, highly scalable service.

-   Collects **any custom log data**, including:
    -   Application Logs
        -   Example: CloudWatch Logs can track the number of errors occur in our application logs and send us a notification whenever the rate of errors exceeds a certain threshold specified.
    -   Nginx Logs
    -   Lambda Logs

### Metrics

-   Represents a **time-ordered set of data points**.
-   Example: Monitoring **Memory Usage**.

### Events

-   Triggers an event based on a condition.
    -   Example: Take a snapshot of a server every hour (**Now known as Amazon EventBridge**).

### Alarms

-   Triggers notifications based on **metrics that breach a defined threshold**.

### Dashboards

-   Create **visualizations** based on metrics.

### ServiceLens

-   Visualize and analyze the **health, performance, and availability** of your app in a single place.

### Container Insights

-   Collects, aggregates, and summarizes **metrics and logs** from your **containerized apps** and **microservices**.

### Synthetics

-   Test your **web applications** to see if they are broken.

### Contributor Insights

-   View the **top contributors** impacting the performance of your systems and applications in real-time.

---

👏 **All CloudWatch Services Build Off Of CloudWatch Logs!**

CloudWatch Logs is the foundation for many CloudWatch services, acting as a central repository for storing and filtering log files. These logs are transformed into actionable metrics, enabling advanced features such as triggering alarms when thresholds are breached. These metrics are then utilized to create graphs, allowing us to visualize and improve performance. Additionally, logs support event-driven automation, containerized application monitoring, synthetic testing for web apps, and diagnostic insights to identify top contributors to system performance.
