# Infrastructure as Code Prompt Enhancer
> Transforms basic IaC requests into comprehensive infrastructure definitions with module design, state management, security hardening, and operational best practices.

## Purpose
To convert general Infrastructure as Code prompts into structured IaC specifications that explicitly address tool selection, module architecture, state management, secret handling, testing strategies, and operational patterns before any infrastructure code is written.

## Best For
- Terraform module development and registry design
- CloudFormation template and stack set creation
- Pulumi program architecture and component design
- Ansible playbook and role development
- Kubernetes manifest and Helm chart authoring
- Crossplane composite resource design
- CDK (Cloud Development Kit) application architecture
- Multi-cloud IaC strategy and tooling

## Prompt Enhancer
```text
You are a senior infrastructure engineer specializing in Infrastructure as Code, cloud automation, and DevOps practices. Transform the following request into a structured IaC specification. Follow these steps precisely:

1. TOOL SELECTION AND JUSTIFICATION: Choose the right IaC tool:
   - Primary IaC tool selection (Terraform, CloudFormation, Pulumi, Ansible, CDK)
   - Justification for tool selection over alternatives
   - Provider/plugin requirements and version pinning
   - Language choice (HCL, YAML, Python, TypeScript, Go)
   - State backend selection (S3, GCS, Azure Blob, Terraform Cloud)
   - Module registry strategy (public vs private)
   - Integration with existing toolchain (CI/CD, Git, secrets management)

2. MODULE ARCHITECTURE: Design the code structure:
   - Module hierarchy (root, modules, modules/components)
   - Module boundaries and responsibilities
   - Input/output interface design per module
   - Module versioning strategy (semantic versioning)
   - Module composition patterns (nested modules, wrappers)
   - Shared module library and registry design
   - Example module directory structure with file purposes
   - Testing module boundaries and contract testing

3. STATE MANAGEMENT: Design the state strategy:
   - State backend configuration and security
   - State locking mechanism and conflict resolution
   - State isolation per environment/account/region
   - State import and migration procedures
   - State drift detection and reconciliation
   - State backup and disaster recovery
   - Remote state references and data sources
   - State file encryption and access controls

4. RESOURCE DESIGN: Define infrastructure patterns:
   - Resource naming conventions and tagging strategy
   - Resource dependency management and ordering
   - Lifecycle rules (create, update, destroy, ignore)
   - Count and for_each patterns for resource replication
   - Data source usage for existing resource references
   - Variable validation and type constraints
   - Output design for cross-module communication
   - Resource import for existing infrastructure

5. SECURITY AND SECRETS: Design security controls:
   - Secret management strategy (Vault, SSM, Key Vault)
   - Secret rotation and lifecycle management
   - Sensitive variable marking and output redaction
   - Least-privilege IAM policies for IaC execution
   - Resource policy patterns (security groups, IAM roles)
   - Encryption configuration for all data stores
   - Network security patterns (private endpoints, NACLs)
   - Compliance guardrails and policy-as-code

6. ENVIRONMENT MANAGEMENT: Design multi-environment support:
   - Environment hierarchy (dev, staging, prod, DR)
   - Configuration per environment strategy
   - Variable files and tfvars management
   - Environment promotion workflow
   - Environment isolation (account, VPC, namespace)
   - Ephemeral environment creation and teardown
   - Blue-green and canary deployment patterns
   - Environment-specific resource sizing

7. TESTING STRATEGY: Design IaC testing approach:
   - Static analysis (tflint, cfn-lint, checkov)
   - Unit testing (terratest, pulumitester, cfn-guard)
   - Integration testing (plan + apply in test account)
   - Compliance testing (OPA, Sentinel, Config Rules)
   - Cost estimation testing (infracost)
   - Security scanning (tfsec, cfn-nag, kics)
   - Drift detection testing
   - Destroy/cleanup testing

8. CI/CD INTEGRATION: Design the deployment pipeline:
   - Version control strategy (monorepo vs multi-repo)
   - Pull request workflow and plan output review
   - Approval gates for production changes
   - Automated apply on merge strategy
   - Pipeline stages (validate, plan, apply, verify)
   - Rollback and undo strategies
   - Multi-account deployment orchestration
   - Deployment notifications and audit logging

9. OPERATIONAL PATTERNS: Design for operations:
   - Module documentation and README standards
   - Example configurations and quick-start guides
   - Troubleshooting runbooks for common failures
   - Capacity planning and cost visibility
   - Monitoring and alerting for infrastructure changes
   - Incident response for IaC failures
   - Technical debt tracking and refactoring plan
   - Team onboarding and knowledge transfer

10. MIGRATION AND ADOPTION: Plan the IaC adoption:
    - Existing infrastructure import strategy
    - Terraform state import procedures
    - Code review and knowledge transfer
    - Pilot project and success criteria
    - Phased rollout schedule
    - Training and skill development plan
    - Documentation standards and enforcement
    - Success metrics and adoption tracking

Present the output as a structured IaC specification with code examples (described textually), module diagrams, and operational runbook outlines for each major component.
```

## Example
### Original Prompt
```text
Create Terraform scripts to deploy an EC2 instance with a security group.
```

### Enhanced Prompt
```text
You are a senior infrastructure engineer specializing in Infrastructure as Code, cloud automation, and DevOps practices. Transform the following request into a structured IaC specification. Follow these steps precisely:

1. TOOL SELECTION AND JUSTIFICATION: Choose the right IaC tool:
   - Primary IaC tool selection (Terraform, CloudFormation, Pulumi, Ansible, CDK)
   - Justification for tool selection over alternatives
   - Provider/plugin requirements and version pinning
   - Language choice (HCL, YAML, Python, TypeScript, Go)
   - State backend selection (S3, GCS, Azure Blob, Terraform Cloud)
   - Module registry strategy (public vs private)
   - Integration with existing toolchain (CI/CD, Git, secrets management)

2. MODULE ARCHITECTURE: Design the code structure:
   - Module hierarchy (root, modules, modules/components)
   - Module boundaries and responsibilities
   - Input/output interface design per module
   - Module versioning strategy (semantic versioning)
   - Module composition patterns (nested modules, wrappers)
   - Shared module library and registry design
   - Example module directory structure with file purposes
   - Testing module boundaries and contract testing

3. STATE MANAGEMENT: Design the state strategy:
   - State backend configuration and security
   - State locking mechanism and conflict resolution
   - State isolation per environment/account/region
   - State import and migration procedures
   - State drift detection and reconciliation
   - State backup and disaster recovery
   - Remote state references and data sources
   - State file encryption and access controls

4. RESOURCE DESIGN: Define infrastructure patterns:
   - Resource naming conventions and tagging strategy
   - Resource dependency management and ordering
   - Lifecycle rules (create, update, destroy, ignore)
   - Count and for_each patterns for resource replication
   - Data source usage for existing resource references
   - Variable validation and type constraints
   - Output design for cross-module communication
   - Resource import for existing infrastructure

5. SECURITY AND SECRETS: Design security controls:
   - Secret management strategy (Vault, SSM, Key Vault)
   - Secret rotation and lifecycle management
   - Sensitive variable marking and output redaction
   - Least-privilege IAM policies for IaC execution
   - Resource policy patterns (security groups, IAM roles)
   - Encryption configuration for all data stores
   - Network security patterns (private endpoints, NACLs)
   - Compliance guardrails and policy-as-code

6. ENVIRONMENT MANAGEMENT: Design multi-environment support:
   - Environment hierarchy (dev, staging, prod, DR)
   - Configuration per environment strategy
   - Variable files and tfvars management
   - Environment promotion workflow
   - Environment isolation (account, VPC, namespace)
   - Ephemeral environment creation and teardown
   - Blue-green and canary deployment patterns
   - Environment-specific resource sizing

7. TESTING STRATEGY: Design IaC testing approach:
   - Static analysis (tflint, cfn-lint, checkov)
   - Unit testing (terratest, pulumitester, cfn-guard)
   - Integration testing (plan + apply in test account)
   - Compliance testing (OPA, Sentinel, Config Rules)
   - Cost estimation testing (infracost)
   - Security scanning (tfsec, cfn-nag, kics)
   - Drift detection testing
   - Destroy/cleanup testing

8. CI/CD INTEGRATION: Design the deployment pipeline:
   - Version control strategy (monorepo vs multi-repo)
   - Pull request workflow and plan output review
   - Approval gates for production changes
   - Automated apply on merge strategy
   - Pipeline stages (validate, plan, apply, verify)
   - Rollback and undo strategies
   - Multi-account deployment orchestration
   - Deployment notifications and audit logging

9. OPERATIONAL PATTERNS: Design for operations:
   - Module documentation and README standards
   - Example configurations and quick-start guides
   - Troubleshooting runbooks for common failures
   - Capacity planning and cost visibility
   - Monitoring and alerting for infrastructure changes
   - Incident response for IaC failures
   - Technical debt tracking and refactoring plan
   - Team onboarding and knowledge transfer

10. MIGRATION AND ADOPTION: Plan the IaC adoption:
    - Existing infrastructure import strategy
    - Terraform state import procedures
    - Code review and knowledge transfer
    - Pilot project and success criteria
    - Phased rollout schedule
    - Training and skill development plan
    - Documentation standards and enforcement
    - Success metrics and adoption tracking

Create Terraform scripts to deploy an EC2 instance with a security group.

Present the output as a structured IaC specification with code examples (described textually), module diagrams, and operational runbook outlines for each major component.
```

## Notes
- The state management section is critical for team collaboration and disaster recovery
- Module design decisions compound over time — force explicit module boundary decisions early
- The testing strategy section is often neglected in IaC — enforce it as a first-class concern
- For regulated environments, expand the security section with specific compliance framework requirements
- The migration section addresses the common challenge of importing existing infrastructure into IaC

## Tags
`infrastructure-as-code` `Terraform` `CloudFormation` `Pulumi` `Ansible` `HCL` `state-management` `module-design` `IaC-testing` `DevOps` `cloud-automation`
