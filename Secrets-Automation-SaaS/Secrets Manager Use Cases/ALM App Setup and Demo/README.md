# Secrets Manager SaaS: ALM Application Setup and Demo 

For Demonstration / Test purposes this API Collection will setup and demo Secrets Management for an application.    

This collection will:
- Organizing Secrets based on an Application
- Create and manage secrets (**Accounts**\Credentials) in a **Safe**
- Create a **Workload** (Machine Identity) for the application
- Grant RBAC access to the associated application **Safe**
- Authenticate and Retrieve **Secrets** using the application **Workload**  

----

**Note:** This project is in beta development
-  Feedback is welcome and changes are expected

----

## Design Intent

This collection and guide are designed to help technical practitioners quickly get up and running with an **end-to-end Secrets Management demo** using minimal inputs and prerequisites. The workflow is intentionally structured as a **step-by-step Bruno Collection**, allowing you to click through the sequence to configure, deploy, and demonstrate core capabilities in a clear and repeatable way.

The design emphasizes visibility into each step of the process, so users can easily understand *what happens*, *why it matters*, and *how it can be automated*. By packaging the flow within an API collection, it also illustrates how the same approach can be extended into **larger automation or orchestration pipelines** using CI/CD or infrastructure-as-code tools.

### Key Design Principles

- **Ease of Use:** Minimal setup and intuitive flow for new users.
- **Repeatability:** Consistent execution across environments and runs.
- **Automation:** Designed to be easily integrated into broader workflows.
- **Clarity:** Transparent actions and clear step-by-step guidance.
- **Openness:** Built to encourage modification, extension, and collaboration.
- **Security:** All secrets are retrieved dynamically at runtime, avoiding hard-coded credentials or clear-text exposure.
- **Segregation of Duties:** Demonstrates clear separation between roles (security admins, developers, automations) to prevent over-privileged access.
- **Least Privilege:** Workload Access scopes are minimized wih policy ensuring that each Identity only has the rights it requires.

## Requirements

- CyberArk SaaS Tenant
  - User Account with System Administrator Role
  - Service Account with System Administrator Role 
- Bruno [usebruno.com](https://usebruno.com)
- This Bruno collection

## Workflow

Open the collection in Bruno
This collection needs to have **Bruno developer settings enabled** to allow for dynamic variable setting and session token collection to work automatically.  

Update the below Bruno collection Environment variables with the following information that can be collected from the SaaS Tenant:
- IspServiceClientId <- Service Account ID (Login Name including @Suffix)
- IspServiceClientSecret <- Service Account Credential (Password) 
- IspTenantId <- Identity ID (Collected From About on the Identity Administration page)   
- IspSubDomain <- Tenant Pre-Fix (Collected from the SaaS URL before .cyberark.cloud: PREFIX.cyberark.cloud) 
- UseCaseAlmAppName <- Give a new custom name of you choice for the application 

### Click Through Setup

Going in Sequence order Top to Bottom Run each API call in the Setup Section 

### Demo Workflow 

Going in Sequence order Top to Bottom Run each API call in the Demo Section 

