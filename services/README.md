# Overview of SaaS Services (un)affected by vulnerability

This page contains an overview of SaaS services (un)affected by the Spring4shell vulnerabilities. NCSC-NL and partners are attempting to maintain a list of all known vulnerable and not vulnerable software. Listed software is paired with specific information regarding which version contains the security fixes and which software still requires fixes. Please note that this vulnerability may also occur in custom software developed within your organisation. These occurrences are not registered in this overview.

| Supplier | Service | Status Spring4shell | Confirmed vulnerable / under investigation / not vulnerable | Notes | Links |
|:---------|:--------|:-------------------:|:--------------------:|:--------------------:|:------|------:|
| AFAS | AFAS | | Not vulnerable | Vendor email: `AFAS Online maakt geen gebruik van Java en/of de kwetsbare bibliotheken die bekend zijn in het kader van 'Spring4Shell'. We volgen de ontwikkelingen en nemen gepaste actie waar nodig.` | |
| Blendr.io | Blendr.io | | Not vulnerable | Vendor email: `Onze code stack steunt niet op java, dus er is geen vulnerability.` | |
| Coveo | Coveo | Not vulnerable | To answer your question, Coveo is unaffected and not vulnerable to the RCE vulnerability in the Spring Framework described here.

However, following our investigation, and due to the nature of the vulnerability, our team is currently performing Spring upgrades everywhere it is used and estimates all necessary work to be completed by April 8th, 2022.

If you have anymore questions or concerns regarding this issue, please let us know. Otherwise, if you are satisfied with this response, please let us know if you comfortable with closing this case. | |
| Hubper | Hubper | | Not vulnerable | Wij hebben vanochtend een eerste analyse gedaan en tot de conclusie gekomen dat wij hier geen last van hebben. Daarna hebben wij de exploit op onszelf uitgevoerd, dit gaf een extra bevestiging.

Ondanks de uitkomst is de mitigratie prima uit te voeren. Dit gaan wij dus ook uitvoeren onder de noemer beter safe then sorry. |
| Jamf | Jamf Pro / Jamf Connect | | Not vulnerable | 10.37.2 and 10.36.4 patched | https://community.jamf.com/t5/jamf-pro/spring4shell-vulnerability/td-p/262584 |
| LucidChart | LucidChart | | Under investigation | - Vulnerability CVE-2022-22963: Spring Cloud Function RCE => Lucid engineers determined that the affected libraries are not used in Lucid’s products

- Another vulnerability was also found in Spring (CVE-2022-22965: Spring Core RCE) => Lucid applied the necessary patches to the single affected system within hours of the patch being made available. Lucid is still investigating impact from third-party software and services that may be affected.


https://lucidchart.zendesk.com/hc/en-us/search?utf8=%E2%9C%93&query=spring4shell

https://lucidchart.zendesk.com/hc/en-us/search?utf8=%E2%9C%93&query=CVE-2022-22963 | |
| Miro | Miro | | Not vulnerable | Miro is aware of the recent vulnerability releases related to Java Spring Framework and associated software components: CVE-2022-22963, CVE-2022-22965.

We'd like to confirm that Miro is not impacted by these specific vulnerabilities and respective attack scenarios.

What has Miro done to address the issue(s)?
— Miro has implemented and validated block rules in its WAF for these CVEs related to the Spring vulnerabilities;
— Miro has reviewed all potentially impacted components, as of now there are no systems affected by this issue;
— As it's a zero-day vulnerability and the nature of the vulnerability is more general, our security and engineering teams are keeping track of related updates and continue to follow our software update procedures. Hope this helps.

More details will be available shortly.| |
| Okta | Okta, Okta Workflows, Auth0, Okta Agents, Okta Access Gateway | | Not vulnerable | | https://sec.okta.com/articles/2022/04/oktas-response-cve-2022-22965-spring4shell | 
| SalesForce | Tableau online | | Under investigation | Schuberg Philis engineers suspect this to be vulnerable as the on premise version has the "right" versions of Tomcat and Spring in the affected configuration. No word from vendor yet | https://security.salesforce.com/security-advisories (returns 404 right now) |
| SentinelOne | SentinelOne | | Not vulnerable | SentinelOne has conducted an internal review to assess the impact of the new zero-day vulnerability in the Spring Core Java framework called Spring4Shell (CVE-2022-22965). With the information published up to this date we have concluded that none of our products are vulnerable to the new Spring4Shell. We will continue to follow the development and research on the vulnerability for published updates and monitor our applications and infrastructure. | |
| Solutions2Share | Teams Manager | Not vulnerable | Vendor email: `"Good morning we don't use that in our application, so there is no impact for us."` | |
| Templafy | Templafy | | Not vulnerable | Thank you for reaching out to Templafy support, I don't believe you need to worry about this vulnerability because Templafy does not have any Java code, neither on our servers, nor deployed to clients. | |
| Unit4 | Intuo (unit4 talent managment) | | Not vulnerable | Vendor email: 
As mentioned yesterday we have contacted our product managers and they have confirmed that we (U4 Talent Management) are not affected by this bug.
Internally we are reviewing if a company wide communication will be provided.

We hope this answers your question, when you agree with this solution please close this ticket on the right side of your screen, if you require additional information please reject the solution and we'll have another look at your case.

When a case is closed you'll be able to fill in a survey to improve our service, we would appreciate it if you would take the time to complete it.

Thanks in advance | |

 