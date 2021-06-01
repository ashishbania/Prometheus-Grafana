# Prometheus-Grafana
---

Let me begin by saying monitoring was never my forte. That was about to change. Let's dive deep into how this duo is the Titan of the observability universe.
The problem statement is as follows: I work on a project with huge data processing demands. This means the system has to be at its performant best round the clock. The major problem I was trying to solve by going down this path was to have a vivid and holistic view of a closed ecosystem platform.
The ask is not nearly simple. There are multiple processes that are active in the system. There are ephemeral jobs, scheduled jobs, API invokes from third parties, etc. What this entails is a nightmare for proper monitoring. One of the basics for monitoring would be to get some primary metrics(both machine and application). Where does Prometheus-Grafana fit the bill?
Most of the apps have support for metrics in Prometheus exposition data format in all newer versions. The version I was grappling to get monitoring established on didn't have OOTB Prometheus implementation. To instrument this setup, I used Prometheus gateway, Prometheus tsdb, and Grafana.
Prometheus TitanFun fact - Prometheus was punished by Zeus for stealing fire for man.

---

Once the Prometheus data is exported in Prometheus TSDB, it's trivially easy to set up datasource in Grafana. Grafana provides a window to run PromQL in the background to generate graphs. Like any powerful language, PromQL has all the aggregation functions available.
Get shocked with rich features. Well, fellas now the fun begins with a plethora of visualization options, like graphs, Gauges, and tables. Observability with Grfana is huge and I would table it for another day.
Below are the reasons why Grafana stands tall.
Reusability: Reusable dashboards
Provisioning: Easy to setup and spin new instance with Docker
Source: Support for multiple datasources
Community: Grafana Labs listens to the community and puts out new releases
Platform: Grafana has a metrics-native platform as opposed to a log-based platform like Kibana.
Hooks: Alerts and integrations to all fun stuffs - Slack and PagerDuty et.al

I hope you had fun reading!
