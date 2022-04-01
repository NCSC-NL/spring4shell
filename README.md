# spring4shell
Operational information regarding the Spring4Shell vulnerability (CVE-2022-22965) in the Spring Core Framework.

* [NCSC-NL advisory](https://www.ncsc.nl/actueel/advisory?id=NCSC-2022-0221)
* [Spring.io announcement of vulnerability](https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement)

## Repository contents

- README.md: contains general information and detection and mitigation measures
- [software/README.md](software/README.md): contains a list of known vulnerable and not vulnerable software. 

**NCSC-NL has published a HIGH/HIGH advisory for the Spring4shell vulnerability. Normally we would update the HIGH/HIGH advisory for vulnerable software packages, however due to the number of expected updates we have created a list of known vulnerable software in the software directory.**

## Mitigation measures

Patches for the following packages are available through [Spring.io](https://spring.io/blog/2022/03/31/spring-framework-rce-early-announcement)
- Spring Framework versions 5.3.18 and 5.2.20
- Spring Boot versions 2.5.12 and 2.6.6

###  Mitigation by vendors

| Vendor | Product | Type | Link |
|:----------------|:----------------|:----------------|:----------------|
| F5 | Big-IP | WAF | https://support.f5.com/csp/article/K24912123 |

## Detection

This table contains an overview of local scanning tools regarding the Spring4shell vulnerability and helps to find vulnerable software.

**NCSC-NL has not verified the scanning tools listed below and therefore cannot guarantee the validity of said tools. However NCSC-NL strives to provide scanning tools from reliable sources.**

| Note     | Links |
|:----------------|:----------------|
|jfrog Spring tools|[https://github.com/jfrog/jfrog-spring-tools](https://github.com/jfrog/jfrog-spring-tools)|
|Hilko Bengen - Local Spring vulnerability scanner|[https://github.com/hillu/local-spring-vuln-scanner](https://github.com/hillu/local-spring-vuln-scanner)|
|Remco Verhoef - Spring4shell scanner|[https://github.com/dtact/spring4shell-scanner](https://github.com/dtact/spring4shell-scanner)|
|Tenable Nessus Spring4shell vulnerability scanner|[https://www.tenable.com/blog/spring4shell-faq-spring-framework-remote-code-execution-vulnerability](https://www.tenable.com/blog/spring4shell-faq-spring-framework-remote-code-execution-vulnerability)|

Next to scanning tools, the following detection rulesets and queries can help to find exploitation/webshells in your network.

| Note     | Links |
|:----------------|:----------------|
|Neo23x0s detection yara rules|[https://github.com/Neo23x0/signature-base/blob/master/yara/expl_spring4shell.yar](https://github.com/Neo23x0/signature-base/blob/master/yara/expl_spring4shell.yar)|
|West-wind Splunk queries|[https://github.com/west-wind/Spring4Shell-Detection](https://github.com/west-wind/Spring4Shell-Detection)|

## Contributions welcome

If you have any additional information to share relevant to the Spring4shell vulnerability, please feel free to open a Pull request. New to this? [Read how to contribute in GitHub's documentation](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files#editing-files-in-another-users-repository).
