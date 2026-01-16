# Telemetry

THIS PAGE IS AI GENERATED. THIS IS FAKE NOT REAL.

## AI prompt

```txt
Create telemetry for NHS Wales DHCW.
- Observability
- Dashboards
- Insights
Format:
- Create plain text that is easy for employees to read.
- Do not create source code.
```

## Telemtry

CONTENTS
1. Introduction to Telemetry
2. Observability Framework
   - Metrics
   - Logs
   - Traces
   - Events
3. Dashboard Specifications
   - Executive Dashboards
   - Operational Dashboards
   - Technical Dashboards
   - Clinical System Dashboards
4. Insights and Analytics
   - Real-Time Insights
   - Trend Analysis
   - Predictive Insights
   - Actionable Recommendations
5. Implementation Guide

## INTRODUCTION TO TELEMETRY

### PURPOSE

Telemetry provides automated collection and transmission of data from DHCW
systems to enable monitoring, troubleshooting, and continuous improvement.
This document defines the telemetry strategy for NHS Wales digital services.

### TELEMETRY PRINCIPLES

Collect Once, Use Many Times
- Instrument systems to capture data that serves multiple purposes:
  operational monitoring, performance analysis, capacity planning,
  and business intelligence.

Context-Rich Data
- Every telemetry data point should include sufficient context
  (timestamp, source, user journey, transaction ID) to enable
  correlation and root cause analysis.

Appropriate Granularity
- Balance detail against storage and processing costs. High-frequency
  data for critical paths, aggregated data for background processes.

Privacy by Design
- Ensure telemetry never captures patient-identifiable information
  unless explicitly required and properly secured. Anonymise and
  aggregate where possible.

Actionable Over Comprehensive
- Prioritise telemetry that drives decisions over data collected
  "just in case." Every metric should have a defined response action.

## OBSERVABILITY FRAMEWORK

Observability enables understanding of system behaviour through external
outputs. DHCW implements the four pillars: Metrics, Logs, Traces, and Events.

### METRICS

Metrics are numeric measurements collected at regular intervals, providing
quantitative insight into system health and performance.

INFRASTRUCTURE METRICS

Metric: CPU Utilisation
- Description:    Percentage of CPU capacity in use
- Collection:     Every 15 seconds
- Aggregation:    1-minute average, 5-minute P95
- Alert Threshold: Warning >70%, Critical >85%
- Retention:      Raw 7 days, aggregated 13 months

Metric: Memory Utilisation
- Description:    Percentage of RAM in use, excluding cache
- Collection:     Every 15 seconds
- Aggregation:    1-minute average
- Alert Threshold: Warning >75%, Critical >90%
- Retention:      Raw 7 days, aggregated 13 months

Metric: Disk I/O
- Description:    Read/write operations per second and throughput
- Collection:     Every 30 seconds
- Aggregation:    5-minute average
- Alert Threshold: Warning >80% of rated IOPS
- Retention:      Raw 7 days, aggregated 13 months

Metric: Network Throughput
- Description:    Bytes in/out per interface
- Collection:     Every 30 seconds
- Aggregation:    5-minute average, hourly totals
- Alert Threshold: Warning >70% bandwidth, Critical >90%
- Retention:      Raw 7 days, aggregated 13 months

APPLICATION METRICS

Metric: Request Rate
- Description:    HTTP requests per second by endpoint
- Collection:     Continuous (counter increment)
- Aggregation:    Per-second rate, 1-minute average
- Alert Threshold: Anomaly detection (±3 standard deviations)
- Retention:      Aggregated 13 months

Metric: Response Time
- Description:    Request duration in milliseconds
- Collection:     Every request (histogram)
- Aggregation:    P50, P90, P95, P99 per minute
- Alert Threshold: P95 >500ms warning, P95 >1000ms critical
- Retention:      Aggregated 13 months

Metric: Error Rate
- Description:    Percentage of requests returning 4xx/5xx status
- Collection:     Every request (counter)
- Aggregation:    Per-minute rate
- Alert Threshold: >1% warning, >5% critical
- Retention:      Aggregated 13 months

Metric: Saturation
- Description:    Queue depths, connection pool usage, thread counts
- Collection:     Every 15 seconds
- Aggregation:    1-minute average and maximum
- Alert Threshold: >80% capacity warning
- Retention:      Aggregated 13 months

BUSINESS METRICS

Metric: Active Users
- Description:    Unique users with active sessions
- Collection:     Session events
- Aggregation:    Real-time count, hourly/daily unique
- Alert Threshold: <50% of expected baseline
- Retention:      Aggregated 25 months

Metric: Transaction Volume
- Description:    Completed business transactions by type
- Collection:     Transaction completion events
- Aggregation:    Per-minute, hourly, daily totals
- Alert Threshold: Anomaly detection from baseline
- Retention:      Aggregated 25 months

Metric: Conversion Rate
- Description:    Percentage of started journeys completed
- Collection:     Journey start and completion events
- Aggregation:    Hourly rate
- Alert Threshold: <80% of baseline
- Retention:      Aggregated 25 months

Metric: Feature Adoption
- Description:    Usage count per feature/function
- Collection:     Feature interaction events
- Aggregation:    Daily active users per feature
- Alert Threshold: None (informational)
- Retention:      Aggregated 25 months

##  LOGS

Logs are timestamped text records of discrete events, providing detailed
context for debugging and audit purposes.

LOG LEVELS AND USAGE
--------------------

Level: FATAL
  Purpose:        System unable to continue operation
  Example:        Database connection permanently failed
  Action:         Immediate page to on-call
  Retention:      36 months

Level: ERROR
  Purpose:        Operation failed but system continues
  Example:        Request failed after retries exhausted
  Action:         Create incident ticket automatically
  Retention:      13 months

Level: WARN
  Purpose:        Unexpected condition, operation succeeded
  Example:        Retry required, deprecated API called
  Action:         Review in daily operations meeting
  Retention:      13 months

Level: INFO
  Purpose:        Normal operational events
  Example:        User login, transaction completed
  Action:         None (baseline for analysis)
  Retention:      90 days

Level: DEBUG
  Purpose:        Detailed diagnostic information
  Example:        Method entry/exit, variable values
  Action:         Enable temporarily for troubleshooting
  Retention:      7 days (when enabled)

Level: TRACE
  Purpose:        Most detailed level, performance impact
  Example:        Every function call, data transformations
  Action:         Enable only in non-production
  Retention:      24 hours (when enabled)

LOG STRUCTURE
-------------

Every log entry must include:

  Timestamp:      ISO 8601 format with milliseconds and timezone
                  Example: 2025-04-15T09:23:45.123Z

  Level:          One of FATAL, ERROR, WARN, INFO, DEBUG, TRACE

  Service:        Name of the originating service
                  Example: welsh-clinical-portal-api

  Instance:       Specific instance identifier
                  Example: wcp-api-prod-3

  Correlation ID: Unique identifier linking related operations
                  Example: req-a1b2c3d4-e5f6-7890

  Message:        Human-readable description of the event

  Context:        Structured data relevant to the event
                  Example: {"userId": "hash123", "endpoint": "/api/results"}

CLINICAL SYSTEM LOGS
--------------------

Additional requirements for clinical systems:

  Audit Trail:    All access to patient data must be logged
  User Identity:  Authenticated user identifier (not PII)
  Action Type:    Create, Read, Update, Delete, Export
  Resource:       Type and identifier of accessed resource
  Outcome:        Success, Failure, Partial
  Reason:         Clinical justification code where applicable

LOG AGGREGATION
---------------

  Collection:     Fluent Bit agents on all hosts
  Transport:      Encrypted TLS to central log service
  Storage:        Elasticsearch cluster with index lifecycle
  Search:         Kibana for interactive exploration
  Alerts:         Log-based alerts for error patterns

--------------------------------------------------------------------------------
2.3 TRACES
--------------------------------------------------------------------------------

Traces follow individual requests across distributed systems, showing the
complete path and timing through multiple services.

TRACE STRUCTURE
---------------

  Trace ID:       Unique identifier for the entire request journey
                  Generated at entry point, propagated through all services

  Span ID:        Unique identifier for a single operation within a trace
                  Each service call creates a new span

  Parent Span:    Reference to the calling span
                  Enables tree reconstruction

  Operation:      Name of the operation
                  Example: "POST /api/appointments/book"

  Duration:       Time taken for the operation in microseconds

  Status:         OK, ERROR, or specific error code

  Attributes:     Key-value pairs providing context
                  Example: http.method, db.statement, user.type

TRACE COLLECTION POINTS
-----------------------

Service Entry:
  Capture:        HTTP method, URL, headers, response status
  Timing:         Total request duration
  Attributes:     Client IP (hashed), user agent, content type

Database Calls:
  Capture:        Query type, table, row count
  Timing:         Query execution time
  Attributes:     Connection pool, read/write replica

External API Calls:
  Capture:        Endpoint, method, response status
  Timing:         Round-trip time
  Attributes:     Retry count, timeout applied

Message Queue:
  Capture:        Queue name, message type, correlation
  Timing:         Time in queue, processing time
  Attributes:     Producer service, consumer service

Cache Operations:
  Capture:        Cache name, operation (get/set/delete)
  Timing:         Operation duration
  Attributes:     Hit/miss, key pattern (not actual key)

SAMPLING STRATEGY
-----------------

Production Environment:
  Baseline:       1% of all requests sampled
  Errors:         100% of error traces captured
  Slow Requests:  100% of requests >2 seconds captured
  Clinical:       100% of clinical data access traced

Non-Production:
  All Traces:     100% sampling for debugging

Adaptive Sampling:
  High Load:      Reduce to 0.1% when >10,000 req/sec
  Incidents:      Increase to 100% during active incidents

TRACE RETENTION
---------------

  Full Detail:    7 days
  Aggregated:     90 days (service-to-service latency summaries)
  Error Traces:   13 months

--------------------------------------------------------------------------------
2.4 EVENTS
--------------------------------------------------------------------------------

Events are significant occurrences that provide context for metric changes
and log patterns, enabling correlation and impact analysis.

SYSTEM EVENTS
-------------

Event: Deployment
  Data Captured:  Service name, version, environment, deployer
  Correlation:    Overlay on metric graphs
  Retention:      25 months

Event: Configuration Change
  Data Captured:  Service, parameter, old value, new value, changer
  Correlation:    Link to subsequent metric shifts
  Retention:      25 months

Event: Scaling Event
  Data Captured:  Service, previous count, new count, trigger reason
  Correlation:    Capacity metrics
  Retention:      13 months

Event: Certificate Renewal
  Data Captured:  Domain, old expiry, new expiry
  Correlation:    TLS error logs
  Retention:      25 months

OPERATIONAL EVENTS
------------------

Event: Incident Created
  Data Captured:  Incident ID, priority, affected services, summary
  Correlation:    Error rates, user impact metrics
  Retention:      36 months

Event: Incident Resolved
  Data Captured:  Incident ID, resolution time, root cause category
  Correlation:    Service restoration timing
  Retention:      36 months

Event: Maintenance Window
  Data Captured:  Start time, end time, affected services, type
  Correlation:    Suppress alerts, contextualise availability
  Retention:      25 months

Event: Failover
  Data Captured:  Service, from instance, to instance, trigger
  Correlation:    Availability metrics, latency changes
  Retention:      25 months

BUSINESS EVENTS
---------------

Event: Campaign Launch
  Data Captured:  Campaign name, expected volume, start time
  Correlation:    Traffic patterns, capacity utilisation
  Retention:      25 months

Event: Partner Onboarding
  Data Captured:  Partner ID, services enabled, go-live date
  Correlation:    New traffic sources, integration errors
  Retention:      25 months

Event: Feature Release
  Data Captured:  Feature name, rollout percentage, target users
  Correlation:    Feature adoption metrics, error rates
  Retention:      25 months

Event: Policy Change
  Data Captured:  Policy type, effective date, affected users
  Correlation:    User behaviour changes
  Retention:      25 months

================================================================================
3. DASHBOARD SPECIFICATIONS
================================================================================

Dashboards transform telemetry data into visual insights for different
audiences. Each dashboard type serves specific decision-making needs.

--------------------------------------------------------------------------------
3.1 EXECUTIVE DASHBOARDS
--------------------------------------------------------------------------------

Purpose: Strategic oversight for senior leadership
Audience: CEO, Executive Directors, Board Members
Refresh Rate: Daily summary, weekly trends
Access: Executive leadership group

DASHBOARD: Service Health Summary

Panel 1: Overall System Status
  Visualisation:  Traffic light indicator (Green/Amber/Red)
  Data Source:    Composite health score from all services
  Drill-Down:     Click to see affected services

Panel 2: Key Service Availability (30 Days)
  Visualisation:  Percentage gauge with trend arrow
  Data Source:    Uptime calculation from monitoring
  Target Line:    99.9% SLA threshold displayed

Panel 3: User Satisfaction Trend
  Visualisation:  Line chart (12-month view)
  Data Source:    In-app feedback scores, support survey
  Comparison:     Previous year overlay

Panel 4: Incident Summary
  Visualisation:  Bar chart by severity
  Data Source:    Incident management system
  Time Range:     Current month vs previous month

DASHBOARD: Digital Adoption

Panel 1: Active Users
  Visualisation:  Big number with percentage change
  Data Source:    Unique authenticated users
  Comparison:     Same period last year

Panel 2: Transaction Volumes
  Visualisation:  Stacked area chart by transaction type
  Data Source:    Completed transactions
  Time Range:     12-month rolling

Panel 3: Channel Distribution
  Visualisation:  Pie chart (App vs Web vs API)
  Data Source:    Request source analysis
  Trend:          Quarter-on-quarter shift

Panel 4: Health Board Adoption
  Visualisation:  Map of Wales with heat overlay
  Data Source:    Usage by Health Board geography
  Metric:         Transactions per 1,000 population

DASHBOARD: Financial Performance

Panel 1: Cost per Transaction
  Visualisation:  Line chart with target line
  Data Source:    Infrastructure costs / transaction volume
  Time Range:     12-month trend

Panel 2: Infrastructure Spend
  Visualisation:  Stacked bar (compute, storage, network, licences)
  Data Source:    Cloud billing, licence management
  Comparison:     Budget vs actual

Panel 3: Efficiency Ratio
  Visualisation:  Gauge showing transactions per £1,000 spent
  Data Source:    Calculated from volume and cost
  Target:         Year-on-year improvement target

Panel 4: Capacity Utilisation
  Visualisation:  Bullet chart by resource type
  Data Source:    Average utilisation metrics
  Ranges:         Under-utilised, optimal, over-utilised

--------------------------------------------------------------------------------
3.2 OPERATIONAL DASHBOARDS
--------------------------------------------------------------------------------

Purpose: Day-to-day service management
Audience: Service Managers, Operations Team, Service Desk
Refresh Rate: Real-time (30-second refresh)
Access: Operations and support staff

DASHBOARD: Live Service Status

Panel 1: Service Health Matrix
  Visualisation:  Grid of status indicators by service
  Data Source:    Health check endpoints
  Click Action:   Open service detail dashboard

Panel 2: Current Incidents
  Visualisation:  Table with priority, age, assignee
  Data Source:    Incident management system
  Highlight:      P1/P2 incidents prominently displayed

Panel 3: Request Rate (Last Hour)
  Visualisation:  Sparkline per service
  Data Source:    Request counters
  Anomaly:        Highlight unusual patterns

Panel 4: Error Rate (Last Hour)
  Visualisation:  Heatmap by service and time
  Data Source:    Error counters
  Threshold:      Colour intensity indicates severity

DASHBOARD: Capacity Monitor

Panel 1: Infrastructure Utilisation
  Visualisation:  Multi-gauge (CPU, Memory, Disk, Network)
  Data Source:    Infrastructure metrics
  Threshold:      Warning and critical zones marked

Panel 2: Database Performance
  Visualisation:  Connection pool, query latency, locks
  Data Source:    Database metrics
  Alert:          Highlight approaching limits

Panel 3: Queue Depths
  Visualisation:  Bar chart by queue
  Data Source:    Message queue metrics
  Trend:          Growing/shrinking indicator

Panel 4: Auto-Scale Status
  Visualisation:  Timeline of scaling events
  Data Source:    Orchestration platform events
  Context:        Trigger reason displayed

DASHBOARD: User Experience Monitor

Panel 1: Response Time Distribution
  Visualisation:  Histogram of response times
  Data Source:    Request duration metrics
  Percentiles:    P50, P95, P99 lines marked

Panel 2: Geographic Performance
  Visualisation:  Map with latency by region
  Data Source:    Client-side timing, CDN metrics
  Comparison:     Urban vs rural performance

Panel 3: Browser/Device Breakdown
  Visualisation:  Treemap by browser and version
  Data Source:    User agent analysis
  Highlight:      Unsupported browsers flagged

Panel 4: Journey Completion Rates
  Visualisation:  Funnel by user journey type
  Data Source:    Journey start/complete events
  Drop-Off:       Highlight stages with high abandonment

--------------------------------------------------------------------------------
3.3 TECHNICAL DASHBOARDS
--------------------------------------------------------------------------------

Purpose: Deep technical analysis and debugging
Audience: Engineers, Architects, SREs
Refresh Rate: Real-time (10-second refresh)
Access: Technical staff

DASHBOARD: Service Deep Dive (per service)

Panel 1: Request/Response Overview
  Visualisation:  Time series (rate, latency, errors)
  Data Source:    Application metrics
  Time Range:     Selectable (1h, 6h, 24h, 7d)

Panel 2: Dependency Health
  Visualisation:  Service map with latency on edges
  Data Source:    Distributed traces
  Highlight:      Slow or failing dependencies

Panel 3: Resource Consumption
  Visualisation:  Multi-line (CPU, memory, GC, threads)
  Data Source:    Runtime metrics
  Correlation:    Overlay deployment events

Panel 4: Top Endpoints
  Visualisation:  Table sorted by latency or errors
  Data Source:    Request metrics by endpoint
  Drill-Down:     Click to see traces for endpoint

DASHBOARD: Database Performance

Panel 1: Query Performance
  Visualisation:  Top slow queries table
  Data Source:    Query performance logs
  Detail:         Execution plan available

Panel 2: Connection Metrics
  Visualisation:  Pool utilisation over time
  Data Source:    Connection pool metrics
  Threshold:      Max connections marked

Panel 3: Replication Lag
  Visualisation:  Gauge per replica
  Data Source:    Replication metrics
  Alert:          Lag exceeding threshold highlighted

Panel 4: Lock Contention
  Visualisation:  Timeline of blocking events
  Data Source:    Database lock logs
  Analysis:       Blocked queries listed

DASHBOARD: Integration Health

Panel 1: External API Status
  Visualisation:  Status grid per integration partner
  Data Source:    Health checks, response times
  SLA:            Partner SLA compliance indicated

Panel 2: Message Flow
  Visualisation:  Sankey diagram of message routing
  Data Source:    Message queue metrics
  Volume:         Message rates on connections

Panel 3: Integration Errors
  Visualisation:  Error timeline by integration
  Data Source:    Error logs, failed transactions
  Pattern:        Highlight recurring errors

Panel 4: Data Sync Status
  Visualisation:  Table of sync jobs with last run
  Data Source:    Batch job monitoring
  Freshness:      Time since last successful sync

--------------------------------------------------------------------------------
3.4 CLINICAL SYSTEM DASHBOARDS
--------------------------------------------------------------------------------

Purpose: Monitoring clinical system availability and performance
Audience: Clinical Informatics, Health Board IT, DHCW Leadership
Refresh Rate: Real-time for status, hourly for usage
Access: Clinical system stakeholders

DASHBOARD: Welsh Clinical Portal

Panel 1: System Availability
  Visualisation:  Uptime percentage (current month)
  Data Source:    Health check monitoring
  SLA:            99.9% target line displayed

Panel 2: Active Clinical Users
  Visualisation:  Real-time count with 24h comparison
  Data Source:    Session metrics
  Breakdown:      By Health Board

Panel 3: Clinical Action Latency
  Visualisation:  Percentile chart (view record, order, note)
  Data Source:    Transaction timing
  Target:         Clinical usability thresholds

Panel 4: Results Delivery
  Visualisation:  Time from lab release to portal display
  Data Source:    Integration timestamps
  Target:         <15 minutes for critical results

DASHBOARD: GP Systems

Panel 1: National Coverage
  Visualisation:  Map showing system status by practice
  Data Source:    Practice system health checks
  Highlight:      Practices with issues flagged

Panel 2: Prescription Volumes
  Visualisation:  Stacked area (EPS vs paper)
  Data Source:    Prescription transaction logs
  Trend:          Digital prescription growth

Panel 3: Appointment Booking
  Visualisation:  Bookings by channel (in-person, phone, online)
  Data Source:    Appointment system metrics
  Target:         Online booking percentage goal

Panel 4: Integration Status
  Visualisation:  Status of each GP system integration
  Data Source:    Integration health checks
  Detail:         Last successful sync time

DASHBOARD: Patient-Facing Services

Panel 1: NHS Wales App Status
  Visualisation:  Platform status (iOS, Android, Web)
  Data Source:    App health monitoring
  Versions:       Active versions in use

Panel 2: Registration Funnel
  Visualisation:  Funnel from download to verified
  Data Source:    Registration journey events
  Drop-Off:       Identify problematic steps

Panel 3: Feature Usage
  Visualisation:  Bar chart of feature interactions
  Data Source:    Feature telemetry
  Trend:          Week-on-week change

Panel 4: Patient Satisfaction
  Visualisation:  Rating distribution with average
  Data Source:    In-app feedback
  Verbatims:      Recent comments scrolling

================================================================================
4. INSIGHTS AND ANALYTICS
================================================================================

Insights transform raw telemetry into actionable intelligence, enabling
proactive management and continuous improvement.

--------------------------------------------------------------------------------
4.1 REAL-TIME INSIGHTS
--------------------------------------------------------------------------------

ANOMALY DETECTION
-----------------

Insight: Traffic Anomaly
  Detection:      Request rate deviates >3σ from baseline
  Baseline:       Rolling 4-week same-day-of-week average
  Alert:          Immediate notification to operations
  Context:        Possible causes suggested (campaign, incident, attack)

Insight: Latency Spike
  Detection:      P95 latency exceeds 2x normal for >5 minutes
  Baseline:       Rolling 24-hour P95 average
  Alert:          Warning to service owner
  Context:        Correlated events (deployment, dependency change)

Insight: Error Burst
  Detection:      Error rate exceeds threshold for specific error type
  Threshold:      Dynamic based on historical patterns
  Alert:          Create incident if sustained >2 minutes
  Context:        Affected users, sample error traces

Insight: Capacity Pressure
  Detection:      Utilisation approaching limits with demand trend
  Prediction:     Estimated time to saturation
  Alert:          Proactive scaling recommendation
  Context:        Historical patterns at similar times

CORRELATION ENGINE
------------------

Insight: Deployment Impact
  Analysis:       Compare metrics before/after deployment
  Metrics:        Error rate, latency, resource usage
  Verdict:        Improvement, regression, or neutral
  Action:         Auto-recommend rollback if regression detected

Insight: Dependency Impact
  Analysis:       Trace downstream effects of dependency issues
  Detection:      Latency increase correlated with external call
  Blast Radius:   Services and users affected
  Action:         Suggest circuit breaker activation

Insight: User Journey Friction
  Analysis:       Identify steps with high abandonment
  Detection:      Drop-off rate exceeds threshold
  Pattern:        Time of day, device type, user segment
  Action:         Prioritise UX improvement

--------------------------------------------------------------------------------
4.2 TREND ANALYSIS
--------------------------------------------------------------------------------

CAPACITY TRENDS
---------------

Insight: Growth Trajectory
  Analysis:       Linear regression on usage metrics
  Projection:     3-month, 6-month, 12-month forecasts
  Thresholds:     When current capacity will be exceeded
  Recommendation: Capacity increase timing and sizing

Insight: Seasonal Patterns
  Analysis:       Year-over-year comparison
  Patterns:       Daily, weekly, monthly, seasonal cycles
  Preparation:    Advance warning for high-demand periods
  Planning:       Staff and infrastructure readiness

Insight: Efficiency Trend
  Analysis:       Resource usage per transaction over time
  Direction:      Improving, stable, or degrading
  Causes:         Code changes, data growth, usage patterns
  Action:         Optimisation priorities

QUALITY TRENDS
--------------

Insight: Reliability Trend
  Analysis:       Error rate and incident frequency over time
  Metric:         Mean time between failures (MTBF)
  Comparison:     Service-to-service, team-to-team
  Action:         Identify services needing investment

Insight: Performance Trend
  Analysis:       Latency percentiles over weeks/months
  Direction:      Improving, stable, or degrading
  Attribution:    Code changes, load changes, infrastructure
  Action:         Performance optimisation backlog

Insight: User Experience Trend
  Analysis:       Satisfaction scores, completion rates over time
  Correlation:    Technical metrics vs user perception
  Segments:       By user type, geography, device
  Action:         Product improvement priorities

--------------------------------------------------------------------------------
4.3 PREDICTIVE INSIGHTS
--------------------------------------------------------------------------------

FAILURE PREDICTION
------------------

Insight: Disk Exhaustion
  Model:          Linear projection of disk usage growth
  Prediction:     Days until disk full
  Threshold:      Alert when <7 days remaining
  Action:         Automated cleanup or expansion request

Insight: Certificate Expiry
  Tracking:       All TLS certificates with expiry dates
  Prediction:     Certificates expiring in next 30 days
  Alert:          Weekly report, urgent if <7 days
  Action:         Automated renewal where possible

Insight: Resource Exhaustion
  Model:          Time-series forecasting on utilisation
  Prediction:     Probability of capacity breach
  Confidence:     Statistical confidence interval
  Action:         Proactive scaling recommendation

DEMAND PREDICTION
-----------------

Insight: Traffic Forecast
  Model:          Seasonal ARIMA on historical patterns
  Prediction:     Expected request volumes (hourly, daily)
  Accuracy:       Model accuracy metrics displayed
  Action:         Pre-emptive scaling decisions

Insight: Campaign Impact
  Model:          Historical campaign lift factors
  Prediction:     Expected volume increase from planned campaigns
  Input:          Campaign calendar, historical similar events
  Action:         Capacity reservation

Insight: Growth Forecast
  Model:          User growth and engagement trends
  Prediction:     Projected active users and transactions
  Horizon:        Quarterly, annual projections
  Action:         Strategic capacity planning

--------------------------------------------------------------------------------
4.4 ACTIONABLE RECOMMENDATIONS
--------------------------------------------------------------------------------

AUTOMATED RECOMMENDATIONS
-------------------------

Recommendation: Right-Sizing
  Analysis:       Actual utilisation vs provisioned capacity
  Criteria:       Consistently <30% utilised over 30 days
  Suggestion:     Specific instance size reduction
  Savings:        Estimated cost reduction

Recommendation: Performance Optimisation
  Analysis:       Slow query patterns, inefficient code paths
  Criteria:       Repeatedly appearing in slow traces
  Suggestion:     Specific queries or endpoints to optimise
  Impact:         Estimated latency improvement

Recommendation: Reliability Improvement
  Analysis:       Recurring error patterns
  Criteria:       Same root cause multiple incidents
  Suggestion:     Specific fix or architectural change
  Impact:         Estimated incident reduction

Recommendation: Security Hardening
  Analysis:       Detected vulnerabilities, outdated dependencies
  Criteria:       Risk scoring based on severity and exposure
  Suggestion:     Specific patches or configuration changes
  Priority:       Ranked by risk score

INSIGHT REPORTS
---------------

Daily Operations Summary
  Content:        Overnight issues, current status, day's risks
  Audience:       Operations team, service desk
  Delivery:       Email at 07:00, Slack channel
  Actions:        Prioritised list for the day

Weekly Service Review
  Content:        Availability, incidents, trends, capacity
  Audience:       Service managers, technical leads
  Delivery:       Email on Monday, PowerPoint attachment
  Actions:        Items for weekly service review meeting

Monthly Executive Summary
  Content:        SLA performance, user metrics, cost efficiency
  Audience:       Executive team, board members
  Delivery:       Email on 1st of month, PDF report
  Actions:        Strategic decisions, investment priorities

Quarterly Trends Report
  Content:        Long-term trends, predictions, recommendations
  Audience:       Leadership, planning teams
  Delivery:       Presented in quarterly review
  Actions:        Strategic planning input

================================================================================
5. IMPLEMENTATION GUIDE
================================================================================

TECHNOLOGY STACK
----------------

Metrics Collection:
  Agent:          Prometheus node exporter, application SDKs
  Transport:      Prometheus remote write, OTLP
  Storage:        Prometheus (short-term), Cortex (long-term)
  Query:          PromQL

Log Collection:
  Agent:          Fluent Bit
  Transport:      Fluent Bit forward protocol (encrypted)
  Storage:        Elasticsearch
  Query:          Kibana, KQL

Trace Collection:
  Agent:          OpenTelemetry SDK
  Transport:      OTLP (gRPC)
  Storage:        Jaeger or Tempo
  Query:          Jaeger UI, Grafana

Event Collection:
  Sources:        CI/CD pipelines, change management, alerts
  Transport:      Webhook, API push
  Storage:        Event database, Grafana annotations
  Correlation:    Grafana event overlays

Dashboards:
  Platform:       Grafana
  Access:         SSO integration with NHS Wales identity
  Alerting:       Grafana alerting with escalation rules

INSTRUMENTATION STANDARDS
-------------------------

Application Code:
  Metrics:        Use standard metric libraries (Prometheus client)
  Naming:         Snake_case, prefix with service name
  Labels:         Environment, instance, standard dimensions
  Cardinality:    Avoid high-cardinality labels

Logging:
  Format:         Structured JSON
  Levels:         Use appropriate levels consistently
  Context:        Always include correlation ID
  Sensitive:      Never log PII or credentials

Tracing:
  Propagation:    W3C Trace Context standard
  Spans:          Create spans for logical operations
  Attributes:     Add relevant context, avoid PII
  Sampling:       Respect configured sampling rules

DATA GOVERNANCE
---------------

Retention Policy:
  Real-time:      7 days full resolution
  Aggregated:     13 months for operational metrics
  Audit:          36 months for compliance data
  Anonymised:     25 months for analytics

Access Control:
  Executive:      Summary dashboards only
  Operations:     All operational dashboards
  Engineering:    Full access including debug data
  External:       No direct access, reports only

Privacy Requirements:
  No PII:         User IDs must be hashed/anonymised
  Aggregation:    Individual user data aggregated
  Audit Access:   Access to audit logs restricted and logged
  Data Requests:  Process for responding to data subject requests

ROLLOUT PLAN
------------

Phase 1: Foundation (Months 1-2)
  - Deploy collection infrastructure
  - Instrument core services (metrics, logs)
  - Create operational dashboards
  - Establish alerting baseline

Phase 2: Observability (Months 3-4)
  - Enable distributed tracing
  - Create service dependency maps
  - Implement correlation engine
  - Deploy technical dashboards

Phase 3: Insights (Months 5-6)
  - Deploy anomaly detection
  - Create trend analysis reports
  - Implement predictive models
  - Launch executive dashboards

Phase 4: Optimisation (Ongoing)
  - Refine models based on feedback
  - Add service-specific dashboards
  - Expand business metrics
  - Continuous improvement
