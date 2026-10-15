Version: NAFATH-V4
Track: Networking

## Overview
Technology supply chain security involves testing software, data, network, and the connections among them. Software configuration must be kept separate from the software code to minimize the exposure of secrets. AI applications need protection against input and training data attacks. Mobile applications must be tested for security controls. Network providers can leverage RPKI for the validation of the authorized autonomous system that can announce the IP prefix, understanding its limitations. Organizations must also patch software such as Log4j and keep an SBOM to know about the software composition. These practices offer better visibility in responding to security issues. This short essay discusses BGP route hijacking and the limitation of RPKI origin validation.
## Software
Application configuration must be separated from application code. The Twelve-Factor App proposes that environment variables be used for configuration that differs in each deployment. This includes configurations of database connections and services. Secrets like passwords and API keys must not be checked into code or repositories. Separation of configuration will help in making applications portable, while secret management can be used to prevent access.

Resource: The Twelve-Factor App: Config - https://12factor.net/config
## AI
There are two types of adversarial attacks that can be made on a machine-learning model – during inference or training. In evasion, the adversary tampers with the inputs of the model, causing incorrect predictions, but not affecting the training data. Data poisoning is where the training data of the model is tampered with by an adversary, leading the model to learn wrong features. Evasion attacks impact inference, while poisoning impacts learning.

Resource: Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations - https://csrc.nist.gov/pubs/ai/100/2/e2025/final
## Mobile
MASVS stands for the Mobile Application Security Verification Standard which is developed by the Open Web Application Security Project (OWASP). There are various aspects that are covered under MASVS such as secure storage, cryptography, authentication, network communication, interaction with the platform, code quality, resilience, and privacy. This framework can be used by the developers to establish security requirements and by the testers to evaluate a mobile application and detect its vulnerabilities.

Resource: OWASP Mobile Application Security Verification Standard (MASVS) - https://mas.owasp.org/MASVS/
## Networking
When an AS announces a particular IP prefix in a manner that draws the traffic away from the right path, this results in BGP route hijacking. RPKI can be used in this case to ensure that routers validate if the origin AS announcing that particular prefix is authorized to do so through Route Origin Authorizations. The result of validation can be used in the routing policy decisions made by operators. But RPKI origin validation does not validate each and every AS along the path.

Resource: RFC 6811: BGP Prefix Origin Validation - https://www.rfc-editor.org/rfc/rfc6811.html
## Cybersecurity
Log4Shell (CVE-2021-44228) was a high-severity remote code execution vulnerability in the Apache Log4j logging software. In vulnerable versions of Log4j, it was possible for the attacker to initiate an insecure JNDI lookup, gaining the ability to execute malicious code in vulnerable configurations. Log4Shell affected many programs due to the popularity of Log4j. Companies need to identify their vulnerable systems, apply patches to Log4j and related software, assess potential compromise, and watch for vendor patches.

Resource: Mitigation against Log4Shell and other Log4j Vulnerabilities - https://www.cisa.gov/news-events/cybersecurity-advisories/aa21-356a
## Data
Software Bill Of Materials (SBOM) is an official document for software components and their dependencies. This allows organizations to determine libraries within a product and determine if the existing vulnerabilities exist within the component. The Minimum elements according to NTIA include the supplier name, component name, version of component, other unique identifiers, dependencies, author of SBOM data, and time-stamp. SBOM increases visibility within the supply chain; however, it cannot ensure that all components are secure and without vulnerabilities.

Resource: Minimum Elements For a Software Bill of Materials (SBOM) - https://www.ntia.gov/report/2021/minimum-elements-software-bill-materials-sbom
## Misconception in My Track

## Open Question
