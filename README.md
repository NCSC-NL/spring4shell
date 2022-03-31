# spring4shell
Operational information regarding the Spring4Shell vulnerability in the Spring Core Framework.

* [NCSC-NL advisory](https://www.ncsc.nl/actueel/advisory?id=NCSC-2022-0221)

## Repository contents

| Directory                          | Purpose |
|:-----------------------------------|:--------|
| [hunting](hunting/README.md)       | Contains info regarding hunting for exploitation |
| [iocs](iocs/README.md)             | Contains any Indicators of Compromise, such as scanning IPs, etc |
| [detection & mitigation](detection_mitigation/README.md)   | Contains info regarding detection and mitigation, such as regexes for detecting scanning activity and more |
| [scanning](scanning/README.md)     | Contains references to methods and tooling used for scanning for the Spring4shell vulnerability |
| [software](software/README.md)     | Contains a list of known vulnerable and not vulnerable software |
| [tools](tools/README.md)           | Contains a list of tools for automatically parsing info on this repo |

**Please note that these directories are not complete, and are currently being expanded.**

**NCSC-NL has published a HIGH/HIGH advisory for the Spring4shell vulnerability. Normally we would update the HIGH/HIGH advisory for vulnerable software packages, however due to the extensive amounts of expected updates we have created a list of known vulnerable software in the software directory.**

## Contributions welcome

If you have any additional information to share relevant to the Spring4shell vulnerability, please feel free to open a Pull request. New to this? [Read how to contribute in GitHub's documentation](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files#editing-files-in-another-users-repository).
