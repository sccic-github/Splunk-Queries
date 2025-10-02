# Splunk-Queries

## **Baselining**

### **Visualize All Available Sourcetypes**

```
| metadata type=sourcetype
```

## **Configuring Displayed Data**

This query demonstrates how to project only wanted values.

Specifically this query shows eash URL every IP by user agent went to.

```
sourcetype=suricata event_type=http
| stats values(http.http_user_agent), values(http.url), values(src_ip) as server by dest_ip
```
