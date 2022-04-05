# spring4shell
Operational information regarding the Spring4Shell vulnerability (CVE-2022-22965) in the Spring Core Framework.

* [NCSC-NL advisory](https://www.ncsc.nl/actueel/advisory?id=NCSC-2022-0221)
* [Spring.io announcement of vulnerability](https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement)
* [CISA advisory](https://www.cisa.gov/uscert/ncas/current-activity/2022/04/01/spring-releases-security-updates-addressing-spring4shell-and)
* [CERT Bund advisory](https://www.cert-bund.de/advisoryshort/CB-K22-0377%20UPDATE%202)

## Repository contents

- README.md: contains general information and detection and mitigation measures
- [software/README.md](software/README.md): contains a list of known vulnerable and not vulnerable software. 
- [services/README.md](services/README.md): contains a list of known vulnerable and not vulnerable services. 

**NCSC-NL has published a HIGH/HIGH advisory for the Spring4shell vulnerability. Normally we would update a HIGH/HIGH advisory for vulnerable software packages, however due to the expected number of updates we have created a list of known vulnerable software in the software directory.**

## Mitigation measures

Determine if the Spring Core Framework is used in your network. Ensure that deployments of the Spring Core Framework are running a version equal to or greater than 5.3.18 or 5.2.20. Scanning tools are available to help find vulnerable software (Linux and Windows). You can find them below in the section "Detection". Note: the results of these tools do not guarantee that you do not have vulnerable systems. The requirements for the specific vulnerable scenario in the report published by Spring are as follows:
- Running on JDK 9 or higher
- Apache Tomcat as the Servlet container
- Packaged as a traditional WAR and deployed in a standalone Tomcat instance. Typical Spring Boot deployments using an embedded Servlet container or reactive web server are not impacted.
- spring-webmvc or spring-webflux dependency.
- Spring Framework versions 5.3.0 to 5.3.17, 5.2.0 to 5.2.19, and older versions.

Ask your suppliers if they use Spring Core Framework in their applications. Check for critical systems if your vendor has published a patch and deploy this as soon as possible.

If updating is not possible in the short term, check the original [Spring.io advisory](https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement) for possible workarounds. If you are unable to apply these workarounds, we advise to consider shutting down the system until a patch becomes available.

This GitHub page contains a list which is kept up-to-date by NCSC-NL. It can provide you with information about which vendors have published a patch. However, we advise you to monitor information provided by your software vendors as well.
- Check your logs, vulnerable systems and systems that have already been patched for signs of compromise.
- Monitor future updates on Spring4Shell.

###  Mitigation by vendors

| Vendor | Product | Type | Link |
|:----------------|:----------------|:----------------|:----------------|
| Akamai | KSD | WAF | https://www.akamai.com/blog/security/spring-core-spring4shell-zero-day |
| Cisco | AMP | Endpoint | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cisco | Secure Email | Mail protection | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cisco | Secure Firewall | IPS | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cisco | SNORT (SID 30790-30793, 59388, and 59416) | IDS/IPS | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cisco | Malware Analytics | Malware Analysis | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cisco | Secure Web Appliance | WAF | https://blog.talosintelligence.com/2022/03/threat-advisory-spring4shell.html |
| Cloudflare | WAF | WAF | https://blog.cloudflare.com/waf-mitigations-sping4shell/ |
| F5 | Big-IP | WAF | https://support.f5.com/csp/article/K24912123 
| Fortinet | FortiGate | IPS | https://www.fortiguard.com/outbreak-alert/spring4shell-vulnerability|
| Fortinet | FortiSASE | IPS | https://www.fortiguard.com/outbreak-alert/spring4shell-vulnerability |
| Fortinet | FortiADC | IPS | https://www.fortiguard.com/outbreak-alert/spring4shell-vulnerability |
| Fortinet | FortiProxy | IPS | https://www.fortiguard.com/outbreak-alert/spring4shell-vulnerability |
| Fortinet | FortiAnalyzer | Outbreak Detection | https://www.fortiguard.com/outbreak-alert/spring4shell-vulnerability |
| HAProxy | HAProxy | WAF | https://www.haproxy.com/blog/april-2022-cve-2022-22965-spring4shell-remote-code-execution-mitigation/ |
| Symantec | multiple products | IPS | https://symantec-enterprise-blogs.security.com/blogs/threat-intelligence/spring4shell-rce-vuln-java |
| PaloAltoNetworks | Next-Generation Firewall | IPS | https://unit42.paloaltonetworks.com/cve-2022-22965-springshell/ |
| PaloAltoNetworks | Prisma Cloud | Endpoint | https://www.paloaltonetworks.com/blog/prisma-cloud/recent-spring-vulnerabilities/ |
| Trend Micro | Cloud One | IPS | https://success.trendmicro.com/dcx/s/solution/000290730?language=en_US |
| Trend Micro | Deep Discovery Inspector | IDS/IPS | https://success.trendmicro.com/dcx/s/solution/000290730?language=en_US |
| Rapid7 | tCell | WAF | https://www.rapid7.com/blog/post/2022/03/30/spring4shell-zero-day-vulnerability-in-spring-framework/#april120223pmedt |

## Detection

This table contains an overview of local and remote scanning tools regarding the Spring4shell vulnerability and helps to find vulnerable software.

**NCSC-NL has not verified the scanning tools listed below and therefore cannot guarantee the validity of said tools. However NCSC-NL strives to provide scanning tools from reliable sources.**

| Note     | Links |
|:----------------|:----------------|
|jfrog Spring tools|[https://github.com/jfrog/jfrog-spring-tools](https://github.com/jfrog/jfrog-spring-tools)|
|Hilko Bengen - Local Spring vulnerability scanner|[https://github.com/hillu/local-spring-vuln-scanner](https://github.com/hillu/local-spring-vuln-scanner)|
|Remco Verhoef - Spring4shell scanner|[https://github.com/dtact/spring4shell-scanner](https://github.com/dtact/spring4shell-scanner)|
|Tenable Nessus Spring4shell vulnerability scanner|[https://www.tenable.com/blog/spring4shell-faq-spring-framework-remote-code-execution-vulnerability](https://www.tenable.com/blog/spring4shell-faq-spring-framework-remote-code-execution-vulnerability)|
|Qualys Scanner/Cloud Agent |[https://blog.qualys.com/vulnerabilities-threat-research/2022/03/31/spring-framework-zero-day-remote-code-execution-spring4shell-vulnerability](https://blog.qualys.com/vulnerabilities-threat-research/2022/03/31/spring-framework-zero-day-remote-code-execution-spring4shell-vulnerability), [https://github.com/Qualys/spring4scanwin](https://github.com/Qualys/spring4scanwin)|
|Rapid7 Nexpose/InsightVM | [https://docs.rapid7.com/insightvm/spring4shell/](https://docs.rapid7.com/insightvm/spring4shell/)|
|Acunetix | [https://www.acunetix.com/blog/web-security-zone/critical-alert-spring4shell-rce-cve-2022-22965-in-spring/](https://www.acunetix.com/blog/web-security-zone/critical-alert-spring4shell-rce-cve-2022-22965-in-spring/)|
|Nuclei Spring4shell template|[https://github.com/projectdiscovery/nuclei-templates/blob/master/cves/2022/CVE-2022-22965.yaml](https://github.com/projectdiscovery/nuclei-templates/blob/master/cves/2022/CVE-2022-22965.yaml)|
|Whitesource/spring4shell-detect | [https://github.com/whitesource/spring4shell-detect](https://github.com/whitesource/spring4shell-detect)|
|onurgule/S4S-Scanner (Burp extension) | [https://github.com/onurgule/S4S-Scanner](https://github.com/onurgule/S4S-Scanner)|
|gpiechnik2 - Spring4shell scanner (nse script)|[https://github.com/gpiechnik2/nmap-spring4shell](https://github.com/gpiechnik2/nmap-spring4shell)|
|OWASP ZAP Spring4shell rule|[https://www.zaproxy.org/blog/2022-04-04-spring4shell-detection-with-zap/](https://www.zaproxy.org/blog/2022-04-04-spring4shell-detection-with-zap/)|

The following IPs were observed as scanning IPs for this vulnerability: [Scanning IPs](https://www.greynoise.io/viz/tag/spring-core-rce-attempt)

Next to scanning tools, the following detection rulesets and queries can help to find exploitation/webshells in your network.

| Note     | Links |
|:----------------|:----------------|
|Yara rules - Neo23x0|[https://github.com/Neo23x0/signature-base/blob/master/yara/expl_spring4shell.yar](https://github.com/Neo23x0/signature-base/blob/master/yara/expl_spring4shell.yar)|
|Splunk queries - West-wind|[https://github.com/west-wind/Spring4Shell-Detection](https://github.com/west-wind/Spring4Shell-Detection)|
|ET Suricata rules (EXPLOIT Possible SpringCore RCE/Spring4Shell)|[https://rules.emergingthreats.net/open/suricata-5.0/rules/emerging-exploit.rules](https://rules.emergingthreats.net/open/suricata-5.0/rules/emerging-exploit.rules)|

## Contributions welcome

If you have any additional information to share relevant to the Spring4shell vulnerability, please feel free to open a Pull request. New to this? [Read how to contribute in GitHub's documentation](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files#editing-files-in-another-users-repository).
