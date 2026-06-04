# SOC Homelab – Wazuh SIEM Deployment

## Overview

This project documents the deployment and configuration of a Wazuh SIEM environment in a home lab.

The goal of this project was to learn:

* Linux administration
* Docker container management
* SIEM deployment
* Endpoint monitoring
* Threat hunting
* Security event analysis

## Lab Environment

### Host Machine

* Ubuntu 24.04 LTS
* Docker
* Docker Compose

### SIEM Platform

* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard

### Test Systems

* Ubuntu Endpoint
* Kali Linux Attack VM

## Deployment Process

### Step 1: Install Docker

Installed Docker and verified operation.

### Step 2: Deploy Wazuh

Downloaded the Wazuh single-node Docker deployment.

### Step 3: Troubleshooting

Encountered certificate and OpenSearch startup issues.

Problem:

* OpenSearch failed to start.
* Certificate paths were incorrectly configured.

Resolution:

* Regenerated certificates using the Wazuh certificate generator.
* Rebuilt containers.
* Verified Indexer, Manager, and Dashboard services.

### Step 4: Agent Enrollment

Enrolled Ubuntu endpoint into Wazuh.

Verified:

* Agent status Active
* Agent successfully communicating with Manager

## Security Testing

### Nmap Detection

Executed Nmap scans from Kali Linux.

Observed:

* Web server errors
* Nmap user-agent detection
* Wazuh alert generation

### SSH Authentication Failure Detection

Generated failed SSH login attempts from Kali.

Observed:

* Authentication failure logs
* PAM login failure alerts
* SSHD event detection

## Threat Hunting Investigation

Reviewed generated alerts through Wazuh Threat Hunting.

Investigated:

* Source IP
* Agent Name
* Rule ID
* Event Timestamp
* Log Source
* Alert Severity

## Skills Demonstrated

* Linux
* Ubuntu Administration
* Docker
* Docker Compose
* Wazuh SIEM
* Threat Hunting
* Log Analysis
* Security Monitoring
* Endpoint Detection
* SSH Monitoring
* Nmap Detection
* Incident Investigation

## Future Improvements

* Add Windows endpoint
* Add Sysmon integration
* Add vulnerability scanning
* Create custom detection rules
* Build attack simulations
* Add additional Linux endpoints
