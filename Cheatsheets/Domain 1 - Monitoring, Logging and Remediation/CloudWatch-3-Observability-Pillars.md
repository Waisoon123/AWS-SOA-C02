# Pillars of Observability

### What is Observability?

Observability is the capability to continuously generate and discover actionable insights based on signals from the system under observation. In other words, observability allows users to understand a system’s state from its external output and take (corrective) action.

### Problem it addresses

Computer systems are measured by observing low-level signals such as CPU time, memory, disk space, and higher-level and business signals, including API response times, errors, transactions per second, etc.

The observability of a system has a significant impact on its operating and development costs. Observable systems yield meaningful, actionable data to their operators, allowing them to achieve favorable outcomes (faster incident response, increased developer productivity) and less toil and downtime.

### Components of Observability

To obtain observability, we need to use the following:

-   Metrics
-   Logs
-   Traces
    We have to use them together, using them in isolate does not gain us observability.

### Best Practices

**Monitor what matters**

-   The most important consideration with observability is not your servers, network, applications, or customers. It is what matters to you, your business, your project, or your users. (Start first with what your success criteria are.)

**Context propagation and tool selection**

-   Tool selection is important and has a profound difference in how you operate and remediate problems. But worse than choosing a sub-optimal tool is tooling for all basic signal types. For example, collecting basic logs from a workload, but missing transaction traces, leaves you with a gap. The result is an incohesive view of your entire application experiece. All modern approaches to observability depend on "connecting the dots" with application traces.

-   A complete picture of your health and operations requires tools that collect **logs, metrics, and traces**, and then performs correlation, analysis, anomaly detection, dashboarding, alarms and more.

**Collect telemetry from all tiers of your workload**

-   Your applications do not exist in isolation, and interactions with your network infrastructure, cloud providers, internet service providers, SasS partners, and other components both within and outside your control can all impact your outcomes. It is important that you have a holistic view of your entire workload.

-   Focus on integrations where the power of observability is most evident. As a rule, every time one component or service calls another, that call must have at least these data points measured (Duration of request and response, status of the response).

