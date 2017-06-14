# Sink


## http


```
@sink(type="http", publisher.url="<STRING>", basic.auth.username="<STRING>", basic.auth.password="<STRING>", client.truststore.path="<STRING>", client.truststore.pass="<STRING>", @map(type='type', @payload('{{payloadBody}}')))
```


<table>
        <tr>
            <td valign="top">Extension Type</td>
            <td>Sink</td>
        </tr>
        <tr>
            <td valign="top">Description</td>
            <td>This&nbsp;is&nbsp;description&nbsp;for&nbsp;http&nbsp;sink&nbsp;extension.&nbsp;This&nbsp;extension&nbsp;publish&nbsp;the&nbsp;http<br>events&nbsp;in&nbsp;any&nbsp;method&nbsp;types&nbsp;such&nbsp;as&nbsp;POST,&nbsp;GET,&nbsp;PUT,&nbsp;DELETE&nbsp;&nbsp;via&nbsp;http&nbsp;or&nbsp;https<br>protocols.&nbsp;As&nbsp;the&nbsp;additional&nbsp;features&nbsp;this&nbsp;component&nbsp;can&nbsp;provide&nbsp;basic<br>authentication&nbsp;as&nbsp;well&nbsp;as&nbsp;user&nbsp;can&nbsp;publish&nbsp;events&nbsp;using&nbsp;custom&nbsp;client&nbsp;truststore<br>files&nbsp;when&nbsp;publishing&nbsp;events&nbsp;via&nbsp;https&nbsp;protocol.&nbsp;And&nbsp;also&nbsp;user&nbsp;can&nbsp;add&nbsp;any<br>number&nbsp;of&nbsp;headers&nbsp;for&nbsp;each&nbsp;event&nbsp;dynamically.</td>
        </tr>
        <tr>
            <td valign="top">System Parameters</td>
            <td>
                    <ol>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>latency.metrics.enabled</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>true</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>server.bootstrap.socket.timeout</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>15</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>client.bootstrap.socket.timeout</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>15</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.host</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;host.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>0.0.0.0</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.port</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;port.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>9763</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.protocol</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;protocol.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>http</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>https.truststore.file</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;truststore&nbsp;file&nbsp;path.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>${carbon.home}/conf/security/client-truststore.jks</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>https.truststore.pass</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;truststore&nbsp;password.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>wso2carbon</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                    </ol>
            </td>
        </tr>
        <tr>
            <td valign="top">Examples</td>
            <td>
                    <ol>
                            <li>
                                <div>
                                    <pre>@sink(type='http',publisher.url='http://localhost:8009', method='{{method}}',headers='{{headers}}', @map(type='xml' , @payload('{{payloadBody}}')))define stream FooStream (payloadBody String, method string, headers string);
</pre>
                                    Expected&nbsp;input&nbsp;should&nbsp;be&nbsp;in&nbsp;following&nbsp;format:{&lt;events&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&lt;event&gt;<br>&nbsp;&nbsp;&nbsp;<br>&lt;symbol&gt;WSO2&lt;/symbol&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;price&gt;55.6&lt;/price&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&lt;volume&gt;100&lt;/volume&gt;<br>&nbsp;&nbsp;&nbsp;<br>&lt;/event&gt;<br>&lt;/events&gt;<br>,POSTContent-Length:24#Content-Location:USA#Retry-After:120}Above<br>configuration&nbsp;will&nbsp;do&nbsp;a&nbsp;default&nbsp;XML&nbsp;input&nbsp;mapping&nbsp;which&nbsp;will&nbsp;generate&nbsp;as&nbsp;below<br>~Output&nbsp;payload&lt;events&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&lt;event&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&lt;symbol&gt;WSO2&lt;/symbol&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;price&gt;55.6&lt;/price&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&lt;volume&gt;100&lt;/volume&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&lt;/event&gt;<br>&lt;/events&gt;<br>~Output<br>headersContent-Length:24,Content-Location:USA,Retry-After:120,Content-Type:application/xml~Output<br>propertyHTTP_METHOD:POST&nbsp;If&nbsp;you&nbsp;need&nbsp;to&nbsp;use&nbsp;basic&nbsp;authentication,&nbsp;the<br><code>basic.auth.enabled</code>&nbsp;parameter&nbsp;must&nbsp;be&nbsp;set&nbsp;to&nbsp;<code>true</code>.&nbsp;This&nbsp;would&nbsp;also&nbsp;require<br>values&nbsp;to&nbsp;be&nbsp;specified&nbsp;for&nbsp;the&nbsp;<code>basic.auth.username</code>&nbsp;and&nbsp;<code>basic.auth.password</code><br>parameters&nbsp;(e.g.,&nbsp;<code>basic.auth.username='userName'</code>&nbsp;and<br><code>basic.auth.password='passWord'</code>).&nbsp;As&nbsp;a&nbsp;result,the&nbsp;output&nbsp;will&nbsp;also&nbsp;contain&nbsp;the<br><code>Authorization</code>&nbsp;header."
                                </div>
                            </li>
                    </ol>
            </td>
        </tr>
</table>


# Source


## http


```
@source(type="http", receiver.url="<STRING>", basic.auth.enabled="<STRING>", worker.count="<STRING>", server.bootstrap.boss.group.size="<STRING>", server.bootstrap.worker.group.size="<STRING>", @map(type='type', @payload('{{payloadBody}}')))
```


<table>
        <tr>
            <td valign="top">Extension Type</td>
            <td>Source</td>
        </tr>
        <tr>
            <td valign="top">Description</td>
            <td>The&nbsp;HTTP&nbsp;source&nbsp;receives&nbsp;POST&nbsp;requests&nbsp;via&nbsp;HTTP&nbsp;or&nbsp;HTTPS&nbsp;in&nbsp;<code>text</code>,&nbsp;<code>XML</code>&nbsp;or<br><code>JSON</code>&nbsp;format.&nbsp;If&nbsp;required,&nbsp;you&nbsp;can&nbsp;enable&nbsp;basic&nbsp;authentication&nbsp;to&nbsp;ensure&nbsp;that<br>events&nbsp;are&nbsp;received&nbsp;only&nbsp;from&nbsp;users&nbsp;who&nbsp;are&nbsp;authorized&nbsp;to&nbsp;access&nbsp;WSO2&nbsp;DAS.</td>
        </tr>
        <tr>
            <td valign="top">System Parameters</td>
            <td>
                    <ol>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>latency.metrics.enabled</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>true</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>server.bootstrap.socket.timeout</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>15</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>client.bootstrap.socket.timeout</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>Netty&nbsp;transportation&nbsp;property.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>15</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.host</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;host.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>0.0.0.0</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.port</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;port.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>9763</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>default.protocol</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;protocol.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>http</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>https.keystore.file</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;keystore&nbsp;file&nbsp;path.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>${carbon.home}/conf/security/wso2carbon.jks</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>https.keystore.pass</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;keystore&nbsp;pass.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>wso2carbon</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                            <li>
                                <table>
                                    <tr>
                                        <td valign="top">Name</td>
                                        <td>https.cert.pass</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Description</td>
                                        <td>The&nbsp;default&nbsp;cert&nbsp;pass.</td>
                                    <tr>
                                        <td valign="top">Default Value</td>
                                        <td>wso2carbon</td>
                                    </tr>
                                    <tr>
                                        <td valign="top">Possible Parameters</td>
                                        <td>N/A</td>
                                    </tr>
                                </table>
                            </li>
                    </ol>
            </td>
        </tr>
        <tr>
            <td valign="top">Examples</td>
            <td>
                    <ol>
                            <li>
                                <div>
                                    <pre>@source(type='http', receiver.url='http://localhost:9055/endpoints/RecPro', @map(type='xml'))
define stream FooStream (symbol string, price float, volume long);
</pre>
                                    Above&nbsp;source&nbsp;configuration&nbsp;performs&nbsp;a&nbsp;default&nbsp;XML&nbsp;input&nbsp;mapping.&nbsp;The&nbsp;expected<br>input&nbsp;is&nbsp;as&nbsp;follows:&lt;events&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&lt;event&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&lt;symbol&gt;WSO2&lt;/symbol&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;price&gt;55.6&lt;/price&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;<br>&lt;volume&gt;100&lt;/volume&gt;<br>&nbsp;&nbsp;&nbsp;&nbsp;&lt;/event&gt;<br>&lt;/events&gt;<br>If&nbsp;basic&nbsp;authentication&nbsp;is<br>enabled&nbsp;via&nbsp;the&nbsp;<code>basic.auth.enabled='true</code>&nbsp;setting,&nbsp;each&nbsp;input&nbsp;event&nbsp;is&nbsp;also<br>expected&nbsp;to&nbsp;contain&nbsp;the&nbsp;<code>Authorization:'Basic&nbsp;encodeBase64(username:Password)'</code><br>header."
                                </div>
                            </li>
                    </ol>
            </td>
        </tr>
</table>

