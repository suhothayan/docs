# Sink


## http _(sink)_


### Description

This extension publish the http events in any method types such as POST, GET, PUT, DELETE  via http or https
protocols. As the additional features this component can provide basic
authentication as well as user can publish events using custom client truststore
files when publishing events via https protocol. And also user can add any
number of headers for each event dynamically.

### Syntex

```
@sink(type="http", publisher.url="<STRING>", basic.auth.username="<STRING>", basic.auth.password="<STRING>", client.truststore.path="<STRING>", client.truststore.pass="<STRING>", @map(type='type', @payload('{{payloadBody}}')))
```
### System Parameters

|Name	|Description| Default Value| Possible Parameters|
|-------|-----------|--------------|--------------------|
|latency.metrics.enabled|Netty transportation property.|true|N/A|
|server.bootstrap.socket.timeout|Netty transportation property.|15|N/A|
|client.bootstrap.socket.timeout|Netty transportation property.|15|N/A|
|default.host|The default host.|0.0.0.0|N/A|
|https.truststore.file|The default truststore file path.|`${carbon.home}/conf/security/client-truststore.jks`|N/A|

### Examples

#### Example 1
```
@sink(type='http',publisher.url='http://localhost:8009', method='{{method}}',headers='{{headers}}', @map(type='xml' , @payload('{{payloadBody}}')))
define stream FooStream (payloadBody String, method string, headers string);
```
Expected input should be in following format:
```
{<events>
    <event>
        <symbol>WSO2</symbol>
        <price>55.6</price>
        <volume>100</volume>
   </event>
</events>

,POSTContent-Length:24#Content-Location:USA#Retry-After:120}
```
Above configuration will do a default XML input mapping which will generate as below
Output payload
```
<events>
    <event>   
        <symbol>WSO2</symbol>
        <price>55.6</price>
        <volume>100</volume>
    </event>
</events>
```
If you need to use basic authentication, the
basic.auth.enabled parameter must be set to true. This would also require
values to be specified for the basic.auth.username and basic.auth.password
parameters (e.g., `basic.auth.username='userName'` and
`basic.auth.password='passWord'`). As a result,the output will also contain the
Authorization header."

