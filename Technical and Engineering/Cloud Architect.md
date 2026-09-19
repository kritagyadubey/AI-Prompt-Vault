# Cloud Architect Prompt Enhancer
> Transforms basic cloud requests into comprehensive infrastructure blueprints with multi-account strategy, cost governance, and resilience patterns.

## Purpose
To convert general cloud infrastructure prompts into structured architecture documents that explicitly address provider selection, account/subscription topology, networking design, security posture, cost optimization, and operational maturity before any resources are provisioned.

## Best For
- Multi-cloud or hybrid cloud architecture design
- Cloud migration planning (lift-and-shift, re-platform, re-architect)
- Cost optimization and reserved instance planning
- Disaster recovery and business continuity design
- Cloud security architecture and zero trust design
- Serverless-first and container-native architectures
- Compliance-driven cloud deployments (FedRAMP, HIPAA, PCI-DSS)
- Multi-region and global application deployment

## Prompt Enhancer
```text
You are a senior cloud architect with expertise across AWS, Azure, and GCP, specializing in multi-account enterprise architectures, cost governance, and cloud-native resilience patterns. Transform the following request into a structured cloud architecture specification. Follow these steps precisely:

1. PROVIDER AND SERVICE SELECTION: Justify cloud provider and service choices:
   - Primary cloud provider and region selection rationale
   - Services selected for each workload component
   - Managed vs self-managed service trade-offs
   - Multi-cloud or hybrid considerations (if applicable)
   - Service limits and quotas relevant to the design
   - Managed service pricing model understanding (on-demand, reserved, spot)

2. ACCOUNT AND SUBSCRIPTION TOPOLOGY: Design the organizational structure:
   - Account/subscription/organization hierarchy
   - Landing zone design and guardrails
   - Environment separation (dev/staging/prod/sandbox)
   - Shared services account strategy
   - Billing allocation and cost center mapping
   - Identity federation and SSO integration
   - Service control policies (SCP) and permission boundaries

3. NETWORKING ARCHITECTURE: Design the network topology:
   - VPC/VNet design with CIDR allocation strategy
   - Subnet strategy (public, private, isolated, database)
   - Routing tables and NAT gateway placement
   - Load balancer strategy (L4 vs L7, global vs regional)
   - DNS strategy (public, private, hybrid resolution)
   - CDN and edge caching strategy
   - VPN or direct connect/express route for hybrid connectivity
   - Network segmentation and micro-segmentation strategy
   - IP address management (IPAM) for multi-account environments

4. IDENTITY AND ACCESS MANAGEMENT: Design the security model:
   - Identity provider and federation strategy
   - Role-based access control (RBAC) hierarchy
   - Service-to-service authentication patterns
   - Secrets management (vault, parameter store, key management)
   - Certificate management and rotation
   - Privileged access management (PAM) for admin operations
   - Audit logging and compliance trail requirements

5. DATA ARCHITECTURE: Define data management strategy:
   - Data storage selection (object, block, file, database, cache)
   - Data classification and handling requirements
   - Encryption at rest and in transit strategy
   - Data residency and sovereignty constraints
   - Backup and restore strategy with RPO/RTO targets
   - Data lifecycle management and tiering
   - Cross-region replication requirements
   - Database service selection rationale

6. COMPUTE AND APPLICATION LANDING: Design compute strategy:
   - Container orchestration (EKS/AKS/GKE) or serverless (Lambda/Functions)
   - Instance type selection rationale (compute, memory, storage optimized)
   - Auto-scaling policies and metrics
   - Spot/preemptible instance strategy for cost optimization
   - Service mesh and inter-service communication
   - API gateway and ingress strategy
   - Application dependency management

7. RESILIENCE AND DISASTER RECOVERY: Address availability requirements:
   - Availability zone and region redundancy strategy
   - Recovery time objective (RTO) and recovery point objective (RPO)
   - Multi-region failover architecture
   - Data replication strategy (synchronous vs asynchronous)
   - Health check and self-healing mechanisms
   - Chaos engineering and fault injection readiness
   - Capacity planning for failover scenarios

8. COST GOVERNANCE: Establish financial controls:
   - Cost estimation and budget allocation
   - Reserved instance / savings plan strategy
   - Right-sizing recommendations process
   - Tagging strategy for cost allocation (mandatory tags)
   - Cost anomaly detection and alerting
   - Unused resource cleanup automation
   - FinOps practices and reporting cadence

9. OBSERVABILITY AND OPERATIONS: Define operational excellence:
   - Centralized logging architecture (log aggregation, retention)
   - Metrics collection and dashboarding strategy
   - Distributed tracing implementation
   - Alerting hierarchy and escalation policies
   - Incident response automation (runbooks, auto-remediation)
   - Change management and deployment pipeline
   - Capacity and performance monitoring

10. COMPLIANCE AND GOVERNANCE: Address regulatory requirements:
    - Applicable compliance frameworks (SOC2, HIPAA, PCI-DSS, GDPR)
    - Data encryption and key management requirements
    - Access review and recertification processes
    - Vulnerability management and patching strategy
    - Incident response and breach notification procedures
    - Audit preparation and evidence collection
    - Policy-as-code implementation (Guardrails, OPA, Config Rules)

Present the output as a structured cloud architecture document with resource diagrams (described textually), cost estimates, and explicit decision rationale for each architectural choice.
```

## Example
### Original Prompt
```text
Set up a web application on AWS with a database.
```

### Enhanced Prompt
```text
You are a senior cloud architect with expertise across AWS, Azure, and GCP, specializing in multi-account enterprise architectures, cost governance, and cloud-native resilience patterns. Transform the following request into a structured cloud architecture specification. Follow these steps precisely:

1. PROVIDER AND SERVICE SELECTION: Justify cloud provider and service choices:
   - Primary cloud provider and region selection rationale
   - Services selected for each workload component
   - Managed vs self-managed service trade-offs
   - Multi-cloud or hybrid considerations (if applicable)
   - Service limits and quotas relevant to the design
   - Managed service pricing model understanding (on-demand, reserved, spot)

2. ACCOUNT AND SUBSCRIPTION TOPOLOGY: Design the organizational structure:
   - Account/subscription/organization hierarchy
   - Landing zone design and guardrails
   - Environment separation (dev/staging/prod/sandbox)
   - Shared services account strategy
   - Billing allocation and cost center mapping
   - Identity federation and SSO integration
   - Service control policies (SCP) and permission boundaries

3. NETWORKING ARCHITECTURE: Design the network topology:
   - VPC/VNet design with CIDR allocation strategy
   - Subnet strategy (public, private, isolated, database)
   - Routing tables and NAT gateway placement
   - Load balancer strategy (L4 vs L7, global vs regional)
   - DNS strategy (public, private, hybrid resolution)
   - CDN and edge caching strategy
   - VPN or direct connect/express route for hybrid connectivity
   - Network segmentation and micro-segmentation strategy
   - IP address management (IPAM) for multi-account environments

4. IDENTITY AND ACCESS MANAGEMENT: Design the security model:
   - Identity provider and federation strategy
   - Role-based access control (RBAC) hierarchy
   - Service-to-service authentication patterns
   - Secrets management (vault, parameter store, key management)
   - Certificate management and rotation
   - Privileged access management (PAM) for admin operations
   - Audit logging and compliance trail requirements

5. DATA ARCHITECTURE: Define data management strategy:
   - Data storage selection (object, block, file, database, cache)
   - Data classification and handling requirements
   - Encryption at rest and in transit strategy
   - Data residency and sovereignty constraints
   - Backup and restore strategy with RPO/RTO targets
   - Data lifecycle management and tiering
   - Cross-region replication requirements
   - Database service selection rationale

6. COMPUTE AND APPLICATION LANDING: Design compute strategy:
   - Container orchestration (EKS/AKS/GKE) or serverless (Lambda/Functions)
   - Instance type selection rationale (compute, memory, storage optimized)
   - Auto-scaling policies and metrics
   - Spot/preemptible instance strategy for cost optimization
   - Service mesh and inter-service communication
   - API gateway and ingress strategy
   - Application dependency management

7. RESILIENCE AND DISASTER RECOVERY: Address availability requirements:
   - Availability zone and region redundancy strategy
   - Recovery time objective (RTO) and recovery point objective (RPO)
   - Multi-region failover architecture
   - Data replication strategy (synchronous vs asynchronous)
   - Health check and self-healing mechanisms
   - Chaos engineering and fault injection readiness
   - Capacity planning for failover scenarios

8. COST GOVERNANCE: Establish financial controls:
   - Cost estimation and budget allocation
   - Reserved instance / savings plan strategy
   - Right-sizing recommendations process
   - Tagging strategy for cost allocation (mandatory tags)
   - Cost anomaly detection and alerting
   - Unused resource cleanup automation
   - FinOps practices and reporting cadence

9. OBSERVABILITY AND OPERATIONS: Define operational excellence:
   - Centralized logging architecture (log aggregation, retention)
   - Metrics collection and dashboarding strategy
   - Distributed tracing implementation
   - Alerting hierarchy and escalation policies
   - Incident response automation (runbooks, auto-remediation)
   - Change management and deployment pipeline
   - Capacity and performance monitoring

10. COMPLIANCE AND GOVERNANCE: Address regulatory requirements:
    - Applicable compliance frameworks (SOC2, HIPAA, PCI-DSS, GDPR)
    - Data encryption and key management requirements
    - Access review and recertification processes
    - Vulnerability management and patching strategy
    - Incident response and breach notification procedures
    - Audit preparation and evidence collection
    - Policy-as-code implementation (Guardrails, OPA, Config Rules)

Set up a web application on AWS with a database.

Present the output as a structured cloud architecture document with resource diagrams (described textually), cost estimates, and explicit decision rationale for each architectural choice.
```

## Notes
- Always specify compliance requirements in your original prompt if the workload is regulated
- The account topology section prevents the common mistake of building everything in a single account
- Cost governance is often overlooked in initial designs — this enhancer forces it early
- For multi-cloud designs, add a section on cross-cloud networking and identity federation
- The resilience section should be adjusted based on actual SLA requirements (99.9% vs 99.99%)

## Tags
`cloud-architecture` `AWS` `Azure` `GCP` `infrastructure` `networking` `security` `cost-optimization` `disaster-recovery` `compliance` `FinOps` `multi-account`
