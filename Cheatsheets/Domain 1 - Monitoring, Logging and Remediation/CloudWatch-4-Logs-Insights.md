# CloudWatch Log Insights

With **CloudWatch Log Insights**, we can interactively search and analyze our log data in AWS CloudWatch Logs. We can perform queries to help us more efficiently and effectively respond to operational issues. If an issue occurs, we can use CloudWatch Logs Insights to identify potential causes and validate deployed fixes.

CloudWatch Logs Insights automatically discovers fields in logs from AWS services such as Amazon Route 53, AWS Lambda, AWS CloudTrail, and Amazon VPC, and any application or custom log that emits log events as JSON.

CloudWatch Logs Insights are commonly used via the console to do ad-hoc queries against logs groups.

### Advantages

-   more robust filtering then using simple Filter events in a Log Stream
-   Less burdensome then having to export logs to S3 and analyze them via Athena

### Some things to Note!

-   A single request can query up to **50** log groups.
-   Queries time out after **60 minutes**.
-   Query results are available for **7 days**.

### CloudWatch Logs Insights Query Commands

All commands are supported on log groups in the **Standard** log class. Log groups in the **Infrequent Access** log class support all query commands except **pattern, diff, and unmask**.

| ------------- | ------------- |
| display | Displays a specific field or fields in query results. |
| fields | Displays specific fields in query results and supports functions and operations you can use to modify field values and create new fields to use in your query. |
| filter | Filters the query to return only the log events that match one or more conditions. |
| pattern | Automatically clusters your log data into patterns. A pattern is shared text structure that recurs among your log fields. CloudWatch Logs Insights provides ways for you to analyze the patterns found in your log events. |
| diff | Compares the log events found in your requested time period with the log events from a previous time period of equal length, so that you can look for trends and find out if certain log events are new. |
| parse | Extracts data from a log field to create an extracted field that you can process in your query. parse supports both glob mode using wildcards, and regular expressions. |
| sort | Displays the returned log events in ascending (asc) or descending (desc) order. |
| stats | Calculate aggregate statistics using values in the log fields. |
| limit | Specifies a maximum number of log events that you want your query to return. Useful with sort to return "top 20" or "most recent 20" results. |
| dedup | Removes duplicate results based on specific values in fields that you specify. |
| unmask | Displays all the content of a log event that has some content masked because of a data protection policy. |
| Other operations and functions | CloudWatch Logs Insights also supports many comparison, arithmetic, datetime, numeric, string, IP address, and general functions and operations |

### CloudWatch Insights - Discovered Fields

CloudWatch Logs Insights supports different log types. For every log that's sent to a Standard class log group Amazon CloudWatch Logs, CloudWatch Logs Insights automatically generates five system fields:

-   **@message** contains the raw unparsed log event.
-   **@timestamp** contains the event timestamp in the log event's timestamp field.
-   **@ingestionTime** contains the time when CloudWatch Logs received the log event.
-   **@logStream** contains the name of the log stream that the log event was added to.
-   **@log** is a log group identifier in the form of account-id:log-group-name.

For many log types, CloudWatch Logs also automatically discovers the log fields contained in the logs. These automatic discovery fields are shown in the following table:

| Log Type  | Discovered Log Fields |
| ------------- | ------------- |
| Amazon VPC flow logs  | @timestamp, @logStream, @message, accountId, endTime, interfaceId, logStatus, startTime, version, action, bytes, dstAddr, dstPort, packets, protocol, srcAddr, srcPort  |
| Route 53 Logs  | @timestamp, @logStream, @message, edgeLocation, ednsClientSubnet, hostZoneId, protocol, queryName, queryTimestamp, queryType, resolverIp, responseCode, version |
| Lambda Logs  | @timestamp, @logStream, @message, @requestId, @duration, @billedDuration, @type, @maxMemoryUsed, @memorySize  |
| CloudTrail Logs  | eventVersion, eventTime, eventSource, eventName, awsRegion, sourceIPAddress, userAgent ... There are more, do check out the JSON in the CloudTrail events to see the full list. |
| Other Log Types  | @timestamp, @ingestionTime, @logStream, @message, @log  |