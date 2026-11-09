---
title: "Resume"
description: "Hands-on engineering leader with 18+ years in security operations who ships production agentic AI into live customer environments, from tool-calling agents to forward-deployed delivery."
menu: "main"
---

# Professional Summary

Hands-on engineering leader with 18+ years in security operations who ships production agentic AI into live customer environments. As Head of Cyber Threat Engineering & Response at Ostra Security, designed and deployed multi-step, tool-calling LLM agents that triage, enrich, and resolve security alerts, auto-resolving 37% of alert volume under human-in-the-loop guardrails. Builds with the Claude and OpenAI APIs, MCP, and SOAR orchestration in Python. Embeds with customer teams, owns delivery from discovery through production, and feeds field patterns back into the product. Domain fluency across defense, healthcare, and SaaS.

## Core Competencies

- **Agentic AI**: Multi-step tool-calling agents, custom tool integrations, Model Context Protocol (MCP), agent orchestration, prompt and system-prompt engineering, structured outputs, human-in-the-loop guardrails, confidence-based escalation, prompt-injection hardening
- **Platforms & Languages**: Anthropic Claude API, OpenAI API, Python (primary), Bash, REST/JSON integrations, SOAR orchestration, Elastic Security / SIEM, detections-as-code (SIGMA), MITRE ATT&CK, AWS, GCP, Git-based CI/CD
- **Forward-Deployed Delivery**: Customer discovery, embedded implementation in customer environments, end-to-end ownership from prototype to production, executive and technical communication, incident response leadership

---

## Professional Experience

### Cyber Delivery Engineer
**Stealth startup** | *October 2026 - Present*
- Helping organizations adopt AI to strengthen security workflows and make people more effective.

### Head, Cyber Threat Engineering & Response
**Ostra Security** | *July 2025 - October 2026*
- Designed, built, and shipped to production a multi-step, tool-calling LLM agent pipeline for alert triage and verdict analysis, orchestrated through SOAR and fed by Elastic Security detections. Agents query security data, enrich indicators, reason across multiple turns, and decide next actions rather than answering single-shot prompts.
- Delivered measurable production outcomes in a live SOC: agents auto-resolve 37% of alerts, analysts triage ~865 cases per month after automated resolution, and MTTI/MTTR improved 15%.
- Built custom tool integrations in Python with the Claude and OpenAI APIs, exposing SIEM, threat-intel enrichment, and SOAR case management to agents, and adopted MCP to connect models across platforms.
- Implemented human-in-the-loop guardrails for agent output: confidence-based escalation to analysts, review gates before customer-facing actions, and analyst sign-off on all AI-drafted intelligence products. Started building a verdict-feedback loop that captures analyst decisions against agent verdicts to measure accuracy and train the backend analysis engine.
- Developed a custom threat intelligence enrichment application used by analysts during triage and investigation and exposed to agents as a tool. Built a CTI program from the ground up combining automated feed ingestion with AI-assisted analysis and report drafting.
- Served as technical point of contact through monthly check-ins, surfacing automation and detection needs and translating recurring field patterns into pipeline and platform improvements.
- Led migration of production triage operations between SOAR platforms with zero coverage gaps. Operationalized the OSCAR investigation methodology and established the SOC's first metrics tracking and reporting framework.
- Led a globally distributed team spanning SOC operations, detection engineering, threat hunting, and threat intelligence (18x5 hands-on-keyboard coverage). Directed response for 16 incidents in 10 months.

### Principal, Threat & Security Response
**Blackwell Security (Acquired by Ostra Security)** | *October 2023 - July 2025*
- Architected SOAR automation for initial alert triage across a hybrid environment of 150+ on-prem assets and thousands of cloud workloads, the orchestration foundation later extended into the agentic triage pipeline at Ostra.
- Built a detections-as-code pipeline translating SIGMA and NDJSON rules into 5 Elastic SIEM clusters, deploying 65 custom detections across customer environments. Designed AI-driven analytics for healthcare-specific threat patterns.
- Embedded with healthcare customer security teams to tailor detections, automation, and response workflows to their tooling, data, and compliance requirements.
- Conducted data breach investigations end to end, from triage and evidence collection through environment securing and system restoration, ensuring client continuity.
- Created security playbooks and training materials standardizing team response. Authored 10+ customer threat bulletins and blog posts and delivered post-incident root cause analyses with prevention recommendations.

### Senior Cloud Security Engineer
**BigID** | *November 2021 - October 2023*
- Designed and deployed security monitoring across multiple AWS accounts spanning 16 regions, plus GCP and Google Workspace, covering corporate, development, and production environments.
- Built a GitLab CI/CD pipeline deploying Cloud Custodian policies with daily automated updates and merge-triggered deployments. Managed cloud security policy through Git-based change control for auditability.
- Developed custom Python scripts for log retrieval and artifact collection from macOS endpoints and Linux servers used in active investigations.
- Managed vulnerability management for 500+ macOS endpoints. Partnered with the security architect and CISO to implement security practices across customer and production environments.

### Cyber Hunt Analyst / Purple Team / Signatures & E-Policy Lead
**Adapt Forward Cyber Security** | *July 2017 - October 2021*
- Contracted to Naval Information Warfare Center Atlantic, supporting the Defense Health Agency.
- Coordinated 6 to 10 red team engagements as deconfliction POC, testing internal SOC detection and response capabilities.
- Analyzed POC exploit code to develop 10+ detections for Fidelis Network and Endpoint appliances as a Fidelis Threat Research Team contractor.
- Maintained 1,500+ Suricata signatures across 100+ sensors worldwide.
- Developed SIEM detection queries mapped to the MITRE ATT&CK framework, and built Python automation for PCAP retrieval supporting network traffic analysis.

### Cyber Hunt Analyst
**Dependable Global Solutions** | *July 2014 - July 2017*
- Contracted to Naval Information Warfare Center Atlantic, supporting the Defense Health Agency.
- Performed network and host-based intrusion detection for CSSP subscriber sites.
- Conducted real-time correlation and IOC analysis for active threats.
- Provided on-call support during high-severity incidents, including full 24x7 surge coverage.
- Participated in threat hunting operations and wrote initial event detection logic.
- Coordinated with external teams to resolve and document security incidents.

**Key Achievements:**
- Played a key role in reducing incident response time during 24x7 surges.
- Identified and responded to multiple real-world adversary campaigns.
- Created knowledge base articles and IR documentation still in use by the team.
- Contributed to CSSP’s compliance and operational audit success.

### Senior Security Analyst / Deputy SOC Manager
**Defense Point Security** | *April 2014 - July 2014*
- Department of Homeland Security, Headquarters.
- Performed intrusion analysis and IDS event triage for the DHS Headquarters SOC (McAfee NSM). Developed IOCs and automated analysis scripts in Mandiant Intelligent Response for network-wide compromise detection.
- Coordinated case escalation and reporting with the DHS HQ Incident Response team. Provided operational feedback to government management as deputy SOC manager.

### Senior Security Consultant, Professional Services
**HP Enterprise Security Products / ArcSight** | *July 2011 - April 2014*
- Deployed and maintained ArcSight SIEM installations across enterprise customer environments, developing correlation rules, alerting logic, and custom connectors for non-standard data sources tailored to each customer's operations.

---

## Education

### Bachelor of Science in Information Systems Security
**Westwood College** | *2006*

---

## Certifications

- **CompTIA Security+** (Active)
- **GCIA** - GIAC Certified Intrusion Analyst (Expired) *#3643*
- **CCSP** - Certified Cloud Security Professional (Expired) *(#828477)*
- **Security Clearance**: TS/SCI (previously held, inactive)

---

## Community

### Volunteer Organizer & CFP Coordinator
**BSidesDC** | *2013 - 2019*
- Coordinated the Call for Proposals for the BSidesDC Security Conference, implementing a blind evaluation process that kept speaker identities hidden from evaluators to prioritize content quality over notoriety.

---

## Professional Memberships

- **SANS** - SysAdmin, Audit, Network, and Security Institute
- **CompTIA** - Computing Technology Industry Association

---

*References available upon request*

<div style="text-align: center; margin: 2rem 0;">
  <a href="/Seth_Feldman_Resume.pdf" 
     download="Seth_Feldman_Resume.pdf" 
     style="display: inline-block; background: #2563eb; color: white; padding: 12px 24px; text-decoration: none; border-radius: 6px; font-weight: 600; font-size: 16px; box-shadow: 0 2px 4px rgba(0,0,0,0.1); transition: background-color 0.2s ease;">
    📄 Download PDF Resume
  </a>
</div>
