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

## Cybersecurity

## Data

## Misconception in My Track

## Open Question
