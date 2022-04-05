# Overview of SaaS Services (un)affected by vulnerability

This page contains an overview of SaaS services (un)affected by the Spring4shell vulnerabilities. NCSC-NL and partners are attempting to maintain a list of all known vulnerable and not vulnerable software. Listed software is paired with specific information regarding which version contains the security fixes and which software still requires fixes. Please note that this vulnerability may also occur in custom software developed within your organisation. These occurrences are not registered in this overview.

| Supplier | Service | Status Spring4shell | Confirmed vulnerable / under investigation / not vulnerable | Notes | Links |
|:---------|:--------|:-------------------:|:--------------------:|:--------------------:|:------|------:|
| AFAS | AFAS | | Not vulnerable | Vendor email: `AFAS Online maakt geen gebruik van Java en/of de kwetsbare bibliotheken die bekend zijn in het kader van 'Spring4Shell'. We volgen de ontwikkelingen en nemen gepaste actie waar nodig.` | |
| Blendr.io | Blendr.io | | Not vulnerable | Vendor email: `Onze code stack steunt niet op java, dus er is geen vulnerability.` | |
| Coveo | Coveo | Not vulnerable | [vendor email](mails/coveo.md) | |
| Hubper | Hubper | | Not vulnerable | [vendor email](mails/hubper.md) | |
| Jamf | Jamf Pro / Jamf Connect | | Not vulnerable | 10.37.2 and 10.36.4 patched | https://community.jamf.com/t5/jamf-pro/spring4shell-vulnerability/td-p/262584 |
| LucidChart | LucidChart | | Under investigation | [vendor email](mails/lucidchart.md) | |
| Miro | Miro | | Not vulnerable | [vendor email](mails/miro.md) | |
| Okta | Okta, Okta Workflows, Auth0, Okta Agents, Okta Access Gateway | | Not vulnerable | | https://sec.okta.com/articles/2022/04/oktas-response-cve-2022-22965-spring4shell | 
| SalesForce | Tableau online | On premise version uses Spring, Tomcat and JDK9 | Under investigation | Schuberg Philis engineers suspect this to be vulnerable as the on premise version has the "right" versions of Tomcat and Spring in the affected configuration. No word from vendor yet | https://kb.tableau.com/articles/issue/Spring4Shell-CVE-2022-22963-and-CVE-2022-22965 and https://status.salesforce.com/generalmessages/884 |
| SentinelOne | SentinelOne | | Not vulnerable | SentinelOne has conducted an internal review to assess the impact of the new zero-day vulnerability in the Spring Core Java framework called Spring4Shell (CVE-2022-22965). With the information published up to this date we have concluded that none of our products are vulnerable to the new Spring4Shell. We will continue to follow the development and research on the vulnerability for published updates and monitor our applications and infrastructure. | |
| Solutions2Share | Teams Manager | Not vulnerable | Vendor email: `"Good morning we don't use that in our application, so there is no impact for us."` | |
| Templafy | Templafy | | Not vulnerable | Thank you for reaching out to Templafy support, I don't believe you need to worry about this vulnerability because Templafy does not have any Java code, neither on our servers, nor deployed to clients. | |
| Unit4 | Intuo (unit4 talent managment) | | Not vulnerable | [vendor email](mails/unit4.md) | |
