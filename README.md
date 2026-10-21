# Security Research

Vulnerabilities I have reported to the Apache Software Foundation, disclosed through the [ASF security process](https://www.apache.org/security/). **46 CVEs across 15 projects**, 2023 to 2026.

Where a public reproducer exists it is linked. Each one is a minimal, self-contained project that demonstrates the issue and names the release that fixed it.

Across 25 distinct CWEs, two classes dominate: **deserialization of untrusted data** (7) and **server-side request forgery** (7).


## Across the Apache ecosystem: 16 CVEs, 14 projects

| CVE | Component | Class | Fixed in | PoC |
|---|---|---|---|---|
| [CVE-2023-41313](https://www.cve.org/CVERecord?id=CVE-2023-41313) | Doris | `CWE-208` Observable Timing Discrepancy | `1.2.8` | - |
| [CVE-2023-41834](https://www.cve.org/CVERecord?id=CVE-2023-41834) | Flink Stateful Functions | `CWE-74` Improper Neutralization of Special Elements in Output Used by a Downstream Component | `3.3.0` | - |
| [CVE-2023-43123](https://www.cve.org/CVERecord?id=CVE-2023-43123) | Storm | `CWE-200` Exposure of Sensitive Information to an Unauthorized Actor | `2.6.0` | - |
| [CVE-2024-23454](https://www.cve.org/CVERecord?id=CVE-2024-23454) | Hadoop | `CWE-378` Creation of Temporary File With Insecure Permissions | `3.4.0` | - |
| [CVE-2024-23953](https://www.cve.org/CVERecord?id=CVE-2024-23953) | Hive | `CWE-208` Observable Timing Discrepancy | `4.0.0` | - |
| [CVE-2024-29869](https://www.cve.org/CVERecord?id=CVE-2024-29869) | Hive | `CWE-732` Incorrect Permission Assignment for Critical Resource | `4.0.1` | - |
| [CVE-2026-28672](https://www.cve.org/CVERecord?id=CVE-2026-28672) | Ranger | `CWE-77` Improper Neutralization of Special Elements used in a Command | `2.9.0` | [reproducer](https://github.com/oscerd/CVE-2026-28672) |
| [CVE-2026-34476](https://www.cve.org/CVERecord?id=CVE-2026-34476) | SkyWalking MCP | `CWE-918` Server-Side Request Forgery | not published | - |
| [CVE-2026-40005](https://www.cve.org/CVERecord?id=CVE-2026-40005) | IoTDB | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `2.0.10` | - |
| [CVE-2026-40008](https://www.cve.org/CVERecord?id=CVE-2026-40008) | IoTDB | `CWE-470` Use of Externally-Controlled Input to Select Classes or Code | `2.0.10` | - |
| [CVE-2026-40564](https://www.cve.org/CVERecord?id=CVE-2026-40564) | Flink Kubernetes Operator | `CWE-918` Server-Side Request Forgery | `1.15.0` | [reproducer](https://github.com/oscerd/CVE-2026-40564) |
| [CVE-2026-41041](https://www.cve.org/CVERecord?id=CVE-2026-41041) | Gravitino | `CWE-177` Improper Handling of URL Encoding | `1.2.1` | - |
| [CVE-2026-44616](https://www.cve.org/CVERecord?id=CVE-2026-44616) | Zeppelin | `CWE-90` Improper Neutralization of Special Elements used in an LDAP Query | `0.12.1` | - |
| [CVE-2026-49361](https://www.cve.org/CVERecord?id=CVE-2026-49361) | Fluss (incubating) | `CWE-400` Uncontrolled Resource Consumption | not published | - |
| [CVE-2026-63039](https://www.cve.org/CVERecord?id=CVE-2026-63039) | InLong | `CWE-89` Improper Neutralization of Special Elements used in an SQL Command | `2.4.0` | [reproducer](https://github.com/oscerd/CVE-2026-63039) |
| [CVE-2026-64640](https://www.cve.org/CVERecord?id=CVE-2026-64640) | Polaris | `CWE-863` Incorrect Authorization | `1.7.0` | [reproducer](https://github.com/oscerd/CVE-2026-64640) |

## Apache Camel: 30 CVEs

Camel is the project I maintain, so it gets the most scrutiny. The dominant pattern is **unfiltered inbound headers reaching a producer's control plane**, plus a long tail of unsafe deserialization in registry and migration paths.

| CVE | Component | Class | Fixed in | PoC |
|---|---|---|---|---|
| [CVE-2024-23114](https://www.cve.org/CVERecord?id=CVE-2024-23114) | Camel | `CWE-502` Deserialization of Untrusted Data | `3.21.4`, `3.22.1`, `4.0.4`, `4.4.0` | - |
| [CVE-2026-23552](https://www.cve.org/CVERecord?id=CVE-2026-23552) | Camel | `CWE-346` Origin Validation Error | `4.18.0` | [reproducer](https://github.com/oscerd/CVE-2026-23552) |
| [CVE-2026-25747](https://www.cve.org/CVERecord?id=CVE-2026-25747) | Camel LevelDB | `CWE-502` Deserialization of Untrusted Data | `4.10.9`, `4.14.5`, `4.18.0` | [reproducer](https://github.com/oscerd/CVE-2026-25747) |
| [CVE-2026-27172](https://www.cve.org/CVERecord?id=CVE-2026-27172) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.6`, `4.18.1` | [reproducer](https://github.com/oscerd/CVE-2026-27172) |
| [CVE-2026-40047](https://www.cve.org/CVERecord?id=CVE-2026-40047) | Camel | `CWE-88` Improper Neutralization of Argument Delimiters in a Command | `4.18.3` | [reproducer](https://github.com/oscerd/CVE-2026-40047) |
| [CVE-2026-40048](https://www.cve.org/CVERecord?id=CVE-2026-40048) | Camel PQC | `CWE-502` Deserialization of Untrusted Data | `4.18.2`, `4.20.0` | [reproducer](https://github.com/oscerd/CVE-2026-40048) |
| [CVE-2026-43866](https://www.cve.org/CVERecord?id=CVE-2026-43866) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-43866) |
| [CVE-2026-43867](https://www.cve.org/CVERecord?id=CVE-2026-43867) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-43867) |
| [CVE-2026-46455](https://www.cve.org/CVERecord?id=CVE-2026-46455) | Camel | `CWE-613` Insufficient Session Expiration | `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46455) |
| [CVE-2026-46585](https://www.cve.org/CVERecord?id=CVE-2026-46585) | Camel Lucene | `CWE-639` Authorization Bypass Through User-Controlled Key | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46585) |
| [CVE-2026-46590](https://www.cve.org/CVERecord?id=CVE-2026-46590) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46590) |
| [CVE-2026-46591](https://www.cve.org/CVERecord?id=CVE-2026-46591) | Camel | `CWE-943` Improper Neutralization of Special Elements in Data Query Logic | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46591) |
| [CVE-2026-46592](https://www.cve.org/CVERecord?id=CVE-2026-46592) | Camel | `CWE-441` Unintended Proxy or Intermediary | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46592) |
| [CVE-2026-46726](https://www.cve.org/CVERecord?id=CVE-2026-46726) | Camel Vertx Websocket | `CWE-918` Server-Side Request Forgery | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-46726) |
| [CVE-2026-48203](https://www.cve.org/CVERecord?id=CVE-2026-48203) | Camel | `CWE-918` Server-Side Request Forgery | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-48203) |
| [CVE-2026-48204](https://www.cve.org/CVERecord?id=CVE-2026-48204) | Camel | `CWE-284` Improper Access Control | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-48204) |
| [CVE-2026-48205](https://www.cve.org/CVERecord?id=CVE-2026-48205) | Camel DNS | `CWE-918` Server-Side Request Forgery | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-48205) |
| [CVE-2026-48206](https://www.cve.org/CVERecord?id=CVE-2026-48206) | Camel JIRA | `CWE-639` Authorization Bypass Through User-Controlled Key | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-48206) |
| [CVE-2026-49086](https://www.cve.org/CVERecord?id=CVE-2026-49086) | Camel Dapr | `CWE-441` Unintended Proxy or Intermediary | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-49086) |
| [CVE-2026-49097](https://www.cve.org/CVERecord?id=CVE-2026-49097) | Camel | `CWE-74` Improper Neutralization of Special Elements in Output Used by a Downstream Component | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-49097) |
| [CVE-2026-49098](https://www.cve.org/CVERecord?id=CVE-2026-49098) | Camel | `CWE-74` Improper Neutralization of Special Elements in Output Used by a Downstream Component | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-49098) |
| [CVE-2026-49099](https://www.cve.org/CVERecord?id=CVE-2026-49099) | Camel Salesforce | `CWE-639` Authorization Bypass Through User-Controlled Key | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-49099) |
| [CVE-2026-49365](https://www.cve.org/CVERecord?id=CVE-2026-49365) | Camel | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-49365) |
| [CVE-2026-53913](https://www.cve.org/CVERecord?id=CVE-2026-53913) | Camel Keycloak | `CWE-636` Not Failing Securely | `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-53913) |
| [CVE-2026-55993](https://www.cve.org/CVERecord?id=CVE-2026-55993) | Camel Atmosphere Websocket | `CWE-918` Server-Side Request Forgery | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-55993) |
| [CVE-2026-55994](https://www.cve.org/CVERecord?id=CVE-2026-55994) | Camel Iggy | `CWE-918` Server-Side Request Forgery | `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-55994) |
| [CVE-2026-56139](https://www.cve.org/CVERecord?id=CVE-2026-56139) | Camel Undertow | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.14.8`, `4.18.3`, `4.21.0` | [reproducer](https://github.com/oscerd/CVE-2026-56139) |
| [CVE-2026-56140](https://www.cve.org/CVERecord?id=CVE-2026-56140) | Camel AWS2 SNS | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | - |
| [CVE-2026-63621](https://www.cve.org/CVERecord?id=CVE-2026-63621) | Camel Knative | `CWE-20` Improper Input Validation | `4.14.9`, `4.18.4`, `4.22.0` | [reproducer](https://github.com/oscerd/CVE-2026-63621) |
| [CVE-2026-78329](https://www.cve.org/CVERecord?id=CVE-2026-78329) | Camel Undertow | `CWE-20` Improper Input Validation | `4.14.9`, `4.18.4`, `4.22.0` | [reproducer](https://github.com/oscerd/CVE-2026-78329) |

## Reproducers for issues found by others: 65

As a Camel maintainer I also build reproducers for reports that come in from outside, and for issues found by internal analysis within the project, to confirm the issue and validate the fix. **These are not my findings.** Credit belongs to the reporters named below.

| CVE | Component | Class | Fixed in | Reported by | PoC |
|---|---|---|---|---|---|
| [CVE-2024-22369](https://www.cve.org/CVERecord?id=CVE-2024-22369) | Camel | `CWE-502` Deserialization of Untrusted Data | `3.21.4`, `3.22.1`, `4.0.4`, `4.4.0` | Ziyang Chen from HuaWei Open Source Management Center, Pingtao Wei from HuaWei Open Source Management Center (finder) and Haoran Zhi from HuaWei Open Source Management Center | [reproducer](https://github.com/oscerd/CVE-2024-22369) |
| [CVE-2026-33453](https://www.cve.org/CVERecord?id=CVE-2026-33453) | Camel | `CWE-915` Improperly Controlled Modification of Dynamically-Determined Object Attributes | `4.18.1`, `4.19.0` | Hyunwoo Kim (@v4bel) | [reproducer](https://github.com/oscerd/CVE-2026-33453) |
| [CVE-2026-33454](https://www.cve.org/CVERecord?id=CVE-2026-33454) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.6`, `4.18.1` | Hyunwoo Kim (@v4bel) | [reproducer](https://github.com/oscerd/CVE-2026-33454) |
| [CVE-2026-40022](https://www.cve.org/CVERecord?id=CVE-2026-40022) | Camel Platform HTTP Main | `CWE-288` Authentication Bypass Using an Alternate Path or Channel | `4.14.6`, `4.18.2` | Jihang Yu | [reproducer](https://github.com/oscerd/CVE-2026-40022) |
| [CVE-2026-40453](https://www.cve.org/CVERecord?id=CVE-2026-40453) | Camel JMS | `CWE-178` Improper Handling of Case Sensitivity | `4.14.6`, `4.18.2`, `4.20.0` | Saroj Khadka | [reproducer](https://github.com/oscerd/CVE-2026-40453) |
| [CVE-2026-40473](https://www.cve.org/CVERecord?id=CVE-2026-40473) | Camel Mina | `CWE-502` Deserialization of Untrusted Data | `4.14.6`, `4.18.2`, `4.20.0` | Venkatraman Kumar from Securin | [reproducer](https://github.com/oscerd/CVE-2026-40473) |
| [CVE-2026-40858](https://www.cve.org/CVERecord?id=CVE-2026-40858) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.7`, `4.18.2`, `4.20.0` | Feng Ning from Innora Pte. Ltd. | [reproducer](https://github.com/oscerd/CVE-2026-40858) |
| [CVE-2026-40859](https://www.cve.org/CVERecord?id=CVE-2026-40859) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.8`, `4.18.3`, `4.20.0` | Venkatraman Kumar from Securin | [reproducer](https://github.com/oscerd/CVE-2026-40859) |
| [CVE-2026-40860](https://www.cve.org/CVERecord?id=CVE-2026-40860) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.7`, `4.18.2`, `4.20.0` | Venkatraman Kumar from Securin | [reproducer](https://github.com/oscerd/CVE-2026-40860) |
| [CVE-2026-42527](https://www.cve.org/CVERecord?id=CVE-2026-42527) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.8`, `4.18.3`, `4.21.0` | Venkatraman Kumar from Securin and Yu Bao from Paypal | [reproducer](https://github.com/oscerd/CVE-2026-42527) |
| [CVE-2026-43865](https://www.cve.org/CVERecord?id=CVE-2026-43865) | Camel | `CWE-502` Deserialization of Untrusted Data | `4.14.8`, `4.18.3`, `4.21.0` | gaorenyusi | [reproducer](https://github.com/oscerd/CVE-2026-43865) |
| [CVE-2026-46453](https://www.cve.org/CVERecord?id=CVE-2026-46453) | Camel | `CWE-639` Authorization Bypass Through User-Controlled Key | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46453) |
| [CVE-2026-46454](https://www.cve.org/CVERecord?id=CVE-2026-46454) | Camel | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46454) |
| [CVE-2026-46456](https://www.cve.org/CVERecord?id=CVE-2026-46456) | Camel | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46456) |
| [CVE-2026-46457](https://www.cve.org/CVERecord?id=CVE-2026-46457) | Camel | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46457) |
| [CVE-2026-46584](https://www.cve.org/CVERecord?id=CVE-2026-46584) | Camel Mail | `CWE-200` Exposure of Sensitive Information to an Unauthorized Actor | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46584) |
| [CVE-2026-46587](https://www.cve.org/CVERecord?id=CVE-2026-46587) | Camel | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46587) |
| [CVE-2026-46588](https://www.cve.org/CVERecord?id=CVE-2026-46588) | Camel | `CWE-20` Improper Input Validation | `4.14.8`, `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-46588) |
| [CVE-2026-47323](https://www.cve.org/CVERecord?id=CVE-2026-47323) | Camel | `CWE-178` Improper Handling of Case Sensitivity | `4.14.6`, `4.18.2` | Quac Tran | [reproducer](https://github.com/oscerd/CVE-2026-47323) |
| [CVE-2026-49042](https://www.cve.org/CVERecord?id=CVE-2026-49042) | Camel | `CWE-20` Improper Input Validation | `4.18.3`, `4.21.0` | Yu Bao from PayPal | [reproducer](https://github.com/oscerd/CVE-2026-49042) |
| [CVE-2026-59230](https://www.cve.org/CVERecord?id=CVE-2026-59230) | Camel Mail | `CWE-20` Improper Input Validation | `4.14.9`, `4.18.4`, `4.22.0` | Atuin - Automated Vulnerability Discovery Engine, anciety of Tencent Xuanwu Lab | [reproducer](https://github.com/oscerd/CVE-2026-59230) |
| [CVE-2026-60093](https://www.cve.org/CVERecord?id=CVE-2026-60093) | Camel Azure Storage Datalake | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.14.9`, `4.18.4`, `4.22.0` | n0mi1k and Hiep Nguyen | [reproducer](https://github.com/oscerd/CVE-2026-60093) |
| [CVE-2026-66906](https://www.cve.org/CVERecord?id=CVE-2026-66906) | Camel Azure Storage Blob | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.14.9`, `4.18.4`, `4.22.0` | n0mi1k and Hiep Nguyen | [reproducer](https://github.com/oscerd/CVE-2026-66906) |
| [CVE-2026-66907](https://www.cve.org/CVERecord?id=CVE-2026-66907) | Camel Google Storage | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.14.9`, `4.18.4`, `4.22.0` | n0mi1k | [reproducer](https://github.com/oscerd/CVE-2026-66907) |
| [CVE-2026-66908](https://www.cve.org/CVERecord?id=CVE-2026-66908) | Camel Platform HTTP Main | `CWE-287` Improper Authentication | `4.22.0` | n0mi1k | [reproducer](https://github.com/oscerd/CVE-2026-66908) |
| [CVE-2026-71300](https://www.cve.org/CVERecord?id=CVE-2026-71300) | Camel Atmosphere Websocket | `CWE-20` Improper Input Validation | `4.14.9`, `4.18.4`, `4.22.0` | Barak Srour from Apiiro | [reproducer](https://github.com/oscerd/CVE-2026-71300) |
| [CVE-2026-78162](https://www.cve.org/CVERecord?id=CVE-2026-78162) | Camel Hazelcast | `CWE-502` Deserialization of Untrusted Data | `4.18.5`, `4.22.1`, `4.23.0` | cattier from TCBS and Leon Zlobecki | [reproducer](https://github.com/oscerd/CVE-2026-78162) |
| [CVE-2026-78163](https://www.cve.org/CVERecord?id=CVE-2026-78163) | Camel Docling | `CWE-918` Server-Side Request Forgery | `4.18.5`, `4.22.1`, `4.23.0` | Li Zhiyao (BUPT) | [reproducer](https://github.com/oscerd/CVE-2026-78163) |
| [CVE-2026-78164](https://www.cve.org/CVERecord?id=CVE-2026-78164) | Camel HTTP | `CWE-1336` Improper Neutralization of Special Elements Used in a Template Engine | `4.18.5`, `4.22.1`, `4.23.0` | 1428265354@qq.com | [reproducer](https://github.com/oscerd/CVE-2026-78164) |
| [CVE-2026-78165](https://www.cve.org/CVERecord?id=CVE-2026-78165) | Camel Spring Redis | `CWE-502` Deserialization of Untrusted Data | `4.18.5`, `4.22.1`, `4.23.0` | Leon Zlobecki | [reproducer](https://github.com/oscerd/CVE-2026-78165) |
| [CVE-2026-79983](https://www.cve.org/CVERecord?id=CVE-2026-79983) | Camel FTP | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.18.5`, `4.22.1`, `4.23.0` | Dilrevx from NSSL, SJTU | [reproducer](https://github.com/oscerd/CVE-2026-79983) |
| [CVE-2026-79984](https://www.cve.org/CVERecord?id=CVE-2026-79984) | Camel Mina SFTP | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.18.5`, `4.22.1`, `4.23.0` | Dilrevx from NSSL, SJTU | [reproducer](https://github.com/oscerd/CVE-2026-79984) |
| [CVE-2026-79985](https://www.cve.org/CVERecord?id=CVE-2026-79985) | Camel SMB | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.18.5`, `4.22.1`, `4.23.0` | Dilrevx from NSSL, SJTU | [reproducer](https://github.com/oscerd/CVE-2026-79985) |
| [CVE-2026-79986](https://www.cve.org/CVERecord?id=CVE-2026-79986) | Camel Azure Files | `CWE-22` Improper Limitation of a Pathname to a Restricted Directory | `4.18.5`, `4.22.1`, `4.23.0` | Dilrevx from NSSL, SJTU | [reproducer](https://github.com/oscerd/CVE-2026-79986) |
| [CVE-2026-80312](https://www.cve.org/CVERecord?id=CVE-2026-80312) | Camel OAuth | `CWE-287` Improper Authentication | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-80312) |
| [CVE-2026-80343](https://www.cve.org/CVERecord?id=CVE-2026-80343) | Camel Netty HTTP | `CWE-178` Improper Handling of Case Sensitivity | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-80343) |
| [CVE-2026-80344](https://www.cve.org/CVERecord?id=CVE-2026-80344) | Camel AS2 | `CWE-918` Server-Side Request Forgery | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-80344) |
| [CVE-2026-83531](https://www.cve.org/CVERecord?id=CVE-2026-83531) | Camel Dynamic Router | `CWE-94` Code Injection | `4.18.5`, `4.22.1`, `4.23.0` | Leon Zlobecki | [reproducer](https://github.com/oscerd/CVE-2026-83531) |
| [CVE-2026-84176](https://www.cve.org/CVERecord?id=CVE-2026-84176) | Camel Platform HTTP Vertx | `CWE-942` Permissive Cross-domain Policy with Untrusted Domains | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-84176) |
| [CVE-2026-84178](https://www.cve.org/CVERecord?id=CVE-2026-84178) | Camel OAuth | `CWE-352` Cross-Site Request Forgery | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-84178) |
| [CVE-2026-84180](https://www.cve.org/CVERecord?id=CVE-2026-84180) | Camel Knative | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-84180) |
| [CVE-2026-84181](https://www.cve.org/CVERecord?id=CVE-2026-84181) | Camel Shiro | `CWE-287` Improper Authentication | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-84181) |
| [CVE-2026-85243](https://www.cve.org/CVERecord?id=CVE-2026-85243) | Camel Crypto PGP | `CWE-354` Improper Validation of Integrity Check Value | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85243) |
| [CVE-2026-85245](https://www.cve.org/CVERecord?id=CVE-2026-85245) | Camel Thrift | `CWE-488` Exposure of Data Element to Wrong Session | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85245) |
| [CVE-2026-85246](https://www.cve.org/CVERecord?id=CVE-2026-85246) | Camel Mina | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85246) |
| [CVE-2026-85247](https://www.cve.org/CVERecord?id=CVE-2026-85247) | Camel Knative | `CWE-295` Improper Certificate Validation | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85247) |
| [CVE-2026-85248](https://www.cve.org/CVERecord?id=CVE-2026-85248) | Camel PQC | `CWE-362` Concurrent Execution using Shared Resource with Improper Synchronization | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85248) |
| [CVE-2026-85249](https://www.cve.org/CVERecord?id=CVE-2026-85249) | Camel Tika | `CWE-20` Improper Input Validation | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85249) |
| [CVE-2026-85250](https://www.cve.org/CVERecord?id=CVE-2026-85250) | Camel XPath | `CWE-611` Improper Restriction of XML External Entity Reference | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85250) |
| [CVE-2026-85251](https://www.cve.org/CVERecord?id=CVE-2026-85251) | Camel HTTP | `CWE-200` Exposure of Sensitive Information to an Unauthorized Actor | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85251) |
| [CVE-2026-85254](https://www.cve.org/CVERecord?id=CVE-2026-85254) | Camel Platform HTTP | `CWE-178` Improper Handling of Case Sensitivity | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85254) |
| [CVE-2026-85257](https://www.cve.org/CVERecord?id=CVE-2026-85257) | Camel CXF | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85257) |
| [CVE-2026-85260](https://www.cve.org/CVERecord?id=CVE-2026-85260) | Camel MLLP | `CWE-532` Insertion of Sensitive Information into Log File | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85260) |
| [CVE-2026-85296](https://www.cve.org/CVERecord?id=CVE-2026-85296) | Camel AS2 | `CWE-488` Exposure of Data Element to Wrong Session | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85296) |
| [CVE-2026-85300](https://www.cve.org/CVERecord?id=CVE-2026-85300) | Camel PQC | `CWE-276` Incorrect Default Permissions | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85300) |
| [CVE-2026-85301](https://www.cve.org/CVERecord?id=CVE-2026-85301) | Camel Keycloak | `CWE-287` Improper Authentication | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85301) |
| [CVE-2026-85312](https://www.cve.org/CVERecord?id=CVE-2026-85312) | Camel Core (Saga) | `CWE-20` Improper Input Validation | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85312) |
| [CVE-2026-85313](https://www.cve.org/CVERecord?id=CVE-2026-85313) | Camel Jetty | `CWE-942` Permissive Cross-domain Policy with Untrusted Domains | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85313) |
| [CVE-2026-85314](https://www.cve.org/CVERecord?id=CVE-2026-85314) | Camel Mail | `CWE-20` Improper Input Validation | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85314) |
| [CVE-2026-85315](https://www.cve.org/CVERecord?id=CVE-2026-85315) | Camel gRPC | `CWE-209` Generation of Error Message Containing Sensitive Information | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85315) |
| [CVE-2026-85316](https://www.cve.org/CVERecord?id=CVE-2026-85316) | Camel Platform HTTP | `CWE-1220` Insufficient Granularity of Access Control | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85316) |
| [CVE-2026-85317](https://www.cve.org/CVERecord?id=CVE-2026-85317) | Camel HTTP | `CWE-524` Use of Cache Containing Sensitive Information | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-85317) |
| [CVE-2026-88789](https://www.cve.org/CVERecord?id=CVE-2026-88789) | Camel Quarkus XSLT (Xalan) | `CWE-611` Improper Restriction of XML External Entity Reference | `3.33.3`, `3.40.0` | Apache Camel internal analysis, using Claude Security Tool | [reproducer](https://github.com/oscerd/CVE-2026-88789) |
| [CVE-2026-88901](https://www.cve.org/CVERecord?id=CVE-2026-88901) | Camel Smooks | `CWE-611` Improper Restriction of XML External Entity Reference | `4.18.5`, `4.22.1`, `4.23.0` | h1ei1 | [reproducer](https://github.com/oscerd/CVE-2026-88901) |
| [CVE-2026-91858](https://www.cve.org/CVERecord?id=CVE-2026-91858) | Camel FOP | `CWE-611` Improper Restriction of XML External Entity Reference | `4.18.5`, `4.22.1`, `4.23.0` | Claude Security Scan Tool | [reproducer](https://github.com/oscerd/CVE-2026-91858) |

---

Findings are reported privately to the relevant ASF security team and published only after a fix ships. Reproducers target the vulnerable version and are intended for defenders validating their own exposure.
