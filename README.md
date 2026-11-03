# secbyte-cloud-security-docker-breakout-iam-guardrails-ctf-labs
A practical collection of cybersecurity CTF labs covering Docker container runtime exploits and enterprise multi-cloud posture management.
# Docker Container Escapes, Docker Secrets Management, Multi-Cloud IAM Guardrails & Cloud Incident Response CTF Labs

Welcome to the **Docker Container Escapes, Docker Secrets Management, Multi-Cloud IAM Guardrails & Cloud Incident Response CTF Lab Collection**. This repository serves as an organized, searchable catalog of practical cybersecurity labs hosted on Learn SecByte.

This collection focuses on deep container runtime exploits (Docker breakouts to host root, Swarm/Vault secrets breaches) and enterprise multi-cloud posture management—spanning **Docker Runtime Exploits, Networking & Container Breakouts (Host root escapes via cgroups/Capabilities/Docker sockets, network bridge traversal, image inspection)**, **Docker Secrets Management & Swarm/Vault Security (Docker Swarm secret leaks, HashiCorp Vault integration breaches, runtime environment variable auditing)**, **Multi-Cloud IAM Guardrails & Storage Security (AWS S3 / Azure Blob bucket hunting, IAM over-permissioning, cross-account trust policy abuse)**, and **Cloud Operations, Logging & Incident Response (CloudWatch/CloudTrail audit logging, threat detection alerts, cloud breach containment, and triage workflows)**.

---

## Lab Collection Index

### 1. Docker Runtime Exploits, Container Escapes & Networking
* **Docker Fundamentals: Container Security Lab**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-fundamentals-container-security-lab](https://learn.secbyte.org/ctf/docker-fundamentals-container-security-lab)  
  *Focus:* Understanding Docker runtime isolation boundaries, auditing Linux cgroups and namespaces, and identifying misconfigured container security profiles.

* **Docker Images and Containers: From Inspection to Container Escape**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-images-and-containers-from-inspection-to-container-es](https://learn.secbyte.org/ctf/docker-images-and-containers-from-inspection-to-container-es)  
  *Focus:* Analyzing container image metadata (`docker inspect`), identifying sensitive embedded secrets in build layers, and discovering initial breakout vectors.

* **Docker Networking: Segments, Bridges, and Container Paths**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-networking-segments-bridges-and-container-paths](https://learn.secbyte.org/ctf/docker-networking-segments-bridges-and-container-paths)  
  *Focus:* Auditing Docker network drivers (bridge, host, overlay), capturing inter-container traffic on virtual Ethernet pairs (`veth`), and bypassing container network segmentations.

* **Docker Escape Techniques: Container Breakout Lab**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-escape-techniques-container-breakout-lab](https://learn.secbyte.org/ctf/docker-escape-techniques-container-breakout-lab)  
  *Focus:* Executing container breakouts to host filesystem—exploiting mounted host sockets (`/var/run/docker.sock`), vulnerable kernel drivers, and un-isolated cgroup release notifications.

* **Docker Privilege Escalation Lab: Container Escape to Root**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-privilege-escalation-lab-container-escape-to-root](https://learn.secbyte.org/ctf/docker-privilege-escalation-lab-container-escape-to-root)  
  *Focus:* Escalating container privileges from local user to host root—leveraging dangerous Linux capabilities (`CAP_SYS_ADMIN`, `CAP_NET_ADMIN`), `SUID` binaries on host mounts, and device file injection.

<Image src="image_agent_tag_15830810688650146997" alt="Docker host architecture diagram showing daemon, images, containers, and registry" caption="Docker Daemon Host Architecture & Isolation Topology" />

---

### 2. Docker Secrets Management & Vault Security
* **Docker Secrets Management: Swarm Vault Breach**  
  *Lab Link:* [https://learn.secbyte.org/ctf/docker-secrets-management-swarm-vault-breach](https://learn.secbyte.org/ctf/docker-secrets-management-swarm-vault-breach)  
  *Focus:* Auditing secrets storage across Docker Swarm nodes and HashiCorp Vault sidecars—extracting unencrypted secrets mounted in `/run/secrets/`, recovering memory-dumped API tokens, and hardening secrets injection.

### 3. Multi-Cloud IAM Guardrails, Posture & Storage Security
* **Cloud Storage Security: Bucket & Blob Misconfiguration Hunt**  
  *Lab Link:* [https://learn.secbyte.org/ctf/cloud-storage-security-bucket-blob-misconfiguration-hunt](https://learn.secbyte.org/ctf/cloud-storage-security-bucket-blob-misconfiguration-hunt)  
  *Focus:* Hunting for publicly accessible cloud storage objects—AWS S3 bucket ACL misconfigurations, Azure Blob storage permission leaks, and auditing public read/write permissions.

* **IAM Guardrails: Best Practices**  
  *Lab Link:* [https://learn.secbyte.org/ctf/iam-guardrails-best-practices](https://learn.secbyte.org/ctf/iam-guardrails-best-practices)  
  *Focus:* Enforcing identity least privilege—writing AWS Service Control Policies (SCPs), Azure Policy definitions, blocking wildcards (`"Action": "*"`), and enforcing multi-factor authentication (MFA) enforcement rules.

* **Multi-Cloud Security: Identity Misconfigurations & Incident Response**  
  *Lab Link:* [https://learn.secbyte.org/ctf/multi-cloud-security-identity-misconfigurations-incident-res](https://learn.secbyte.org/ctf/multi-cloud-security-identity-misconfigurations-incident-res)  
  *Focus:* Auditing multi-cloud federated identity trust relationships—detecting cross-account IAM role assumption vulnerabilities, GCP Service Account key exposure, and revoking compromised identity credentials.

<Image src="image_agent_tag_15830810688650149008" alt="Cloud security architecture showing IAM, CASB, MDR, and API security" caption="Enterprise Multi-Cloud Security & Identity Governance Framework" />

---

### 4. Cloud Posture Assessment, Logging & Incident Response
* **Cloud Misconfiguration Assessment: Beacon Harbor**  
  *Lab Link:* [https://learn.secbyte.org/ctf/cloud-misconfiguration-assessment-beacon-harbor](https://learn.secbyte.org/ctf/cloud-misconfiguration-assessment-beacon-harbor)  
  *Focus:* Conducting full cloud posture reviews (CSPM)—identifying exposed management ports (RDP/SSH), open security groups, disabled default encryption, and unaligned compliance baselines.

* **Cloud Watchtower: Logging and Monitoring**  
  *Lab Link:* [https://learn.secbyte.org/ctf/cloud-watchtower-logging-and-monitoring](https://learn.secbyte.org/ctf/cloud-watchtower-logging-and-monitoring)  
  *Focus:* Configuring cloud central logging pipelines—querying AWS CloudTrail, VPC Flow Logs, and CloudWatch log groups to construct forensic attack timelines.

* **Cloud Incident Response: Contain, Triage, Recover**  
  *Lab Link:* [https://learn.secbyte.org/ctf/cloud-incident-response-contain-triage-recover](https://learn.secbyte.org/ctf/cloud-incident-response-contain-triage-recover)  
  *Focus:* Executing cloud-native incident response workflows—isolating compromised EC2/Azure VM instances, taking forensic EBS snapshot images, revoking API tokens, and restoring clean backup states.

---

## Learning Path

### Path A: Docker Security Specialist & Breakout Researcher
1. **Docker Basics & Networking:** Start with [Docker Fundamentals](https://learn.secbyte.org/ctf/docker-fundamentals-container-security-lab), [Docker Inspection](https://learn.secbyte.org/ctf/docker-images-and-containers-from-inspection-to-container-es), and [Docker Networking](https://learn.secbyte.org/ctf/docker-networking-segments-bridges-and-container-paths).
2. **Breakouts & Secrets:** Master escapes in [Docker Escape Techniques](https://learn.secbyte.org/ctf/docker-escape-techniques-container-breakout-lab), [Docker Privilege Escalation](https://learn.secbyte.org/ctf/docker-privilege-escalation-lab-container-escape-to-root), and [Docker Secrets Management](https://learn.secbyte.org/ctf/docker-secrets-management-swarm-vault-breach).

### Path B: Multi-Cloud IAM & Posture Security Engineer
1. **Cloud Storage & IAM:** Audit storage and permissions in [Cloud Storage Security](https://learn.secbyte.org/ctf/cloud-storage-security-bucket-blob-misconfiguration-hunt) and [IAM Guardrails](https://learn.secbyte.org/ctf/iam-guardrails-best-practices).
2. **Posture & Multi-Cloud Identity:** Secure identities in [Multi-Cloud Security](https://learn.secbyte.org/ctf/multi-cloud-security-identity-misconfigurations-incident-res) and [Cloud Misconfiguration Assessment](https://learn.secbyte.org/ctf/cloud-misconfiguration-assessment-beacon-harbor).

### Path C: Cloud Incident Responder & Threat Hunter
1. **Logging & Monitoring:** Analyze cloud audit trails in [Cloud Watchtower](https://learn.secbyte.org/ctf/cloud-watchtower-logging-and-monitoring).
2. **Containment & Triage:** Execute response playbooks in [Cloud Incident Response: Contain, Triage, Recover](https://learn.secbyte.org/ctf/cloud-incident-response-contain-triage-recover).

---

## How to Use the Labs

1. Select a practice scenario from the **Lab Collection Index**.
2. Click the direct link to launch the exercise environment hosted on Learn SecByte.
3. Review scenario directives, Docker daemon configurations, CloudTrail JSON log exports, S3 bucket policies, or IAM role trust definitions.
4. Exploit mounted host Docker sockets, inspect memory dumps for Vault secrets, write AWS SCP policy guardrails, query CloudWatch logs for unauthorized API calls, or isolate compromised cloud virtual machines to capture flags.

---

## Target Audience

* **Cloud Security Engineers & Architects:** Enforce IAM guardrails, write AWS SCPs/Azure policies, audit S3/Blob storage security, and conduct CSPM assessments.
* **Container Security Specialists & Pentesters:** Execute Docker breakouts, analyze Linux kernel capabilities, audit Docker Swarm/Vault secrets, and test network bridge isolation.
* **Cloud Incident Responders & SOC Analysts:** Query CloudTrail/VPC Flow logs, isolate compromised cloud instances, perform EBS snapshot forensics, and execute cloud recovery playbooks.
* **Cybersecurity Students:** Acquire practical hands-on experience in cloud identity management, container escape mechanics, and cloud incident response.

---

## Disclaimer

All lab links provided in this repository direct to official training environments hosted on Learn SecByte. All materials and exercises are provided strictly for educational purposes, defensive skill building, and authorized security research. Unauthorized cloud resource scanning, IAM exploitation, or container breakouts against external production infrastructure without explicit permission is strictly prohibited.
