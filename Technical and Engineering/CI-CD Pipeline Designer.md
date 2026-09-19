# CI/CD Pipeline Designer Prompt Enhancer
> Transforms basic pipeline requests into comprehensive deployment architectures with stage design, quality gates, security scanning, and rollback strategies.

## Purpose
To convert general CI/CD pipeline prompts into structured deployment specifications that explicitly address pipeline architecture, quality gates, security integration, deployment strategies, and operational patterns before any pipeline code is written.

## Best For
- GitHub Actions, GitLab CI/CD, Jenkins pipeline design
- ArgoCD, Flux, and GitOps deployment pipelines
- Multi-stage build and test orchestration
- Deployment strategy implementation (blue-green, canary, rolling)
- Security scanning integration (SAST, DAST, SCA, container scanning)
- Release management and versioning automation
- Infrastructure deployment pipelines (IaC + application)
- Compliance and audit trail for deployments

## Prompt Enhancer
```text
You are a senior DevOps engineer specializing in CI/CD pipeline architecture, deployment strategies, and developer experience optimization. Transform the following request into a structured CI/CD pipeline specification. Follow these steps precisely:

1. PIPELINE ARCHITECTURE: Design the overall pipeline structure:
   - Pipeline trigger strategy (push, PR, schedule, manual)
   - Pipeline stages and their purposes
   - Parallel vs sequential execution decisions
   - Pipeline templates and reusable components
   - Monorepo vs polyrepo pipeline strategy
   - Branch strategy and environment mapping
   - Pipeline as code organization and versioning
   - Cross-pipeline dependencies and orchestration

2. BUILD STAGE: Design the build process:
   - Source code checkout and dependency caching
   - Build environment selection (container, VM, runner)
   - Build matrix strategy (multiple languages, versions, OS)
   - Dependency management and lock file handling
   - Build artifact generation and packaging
   - Build time optimization (caching, parallelism, incremental)
   - Build reproducibility and hermetic builds
   - Build metadata and provenance tracking

3. TEST STAGE: Design the testing pipeline:
   - Test strategy pyramid (unit, integration, e2e)
   - Test execution ordering and prioritization
   - Test parallelization and sharding strategy
   - Test environment provisioning and teardown
   - Test data management and fixtures
   - Test coverage tracking and enforcement
   - Test result reporting and failure analysis
   - Flaky test detection and quarantine

4. QUALITY GATES: Design validation checkpoints:
   - Code quality gates (linting, formatting, complexity)
   - Test coverage thresholds and enforcement
   - Security scanning gates (SAST, DAST, SCA)
   - Dependency vulnerability scanning
   - License compliance checking
   - Performance testing gates (load, stress)
   - Accessibility testing gates (WCAG compliance)
   - Manual approval gates and sign-off requirements

5. SECURITY INTEGRATION: Embed security in the pipeline:
   - SAST (Static Application Security Testing) integration
   - DAST (Dynamic Application Security Testing) integration
   - SCA (Software Composition Analysis) for dependencies
   - Container image scanning and signing
   - Secret scanning and detection
   - Infrastructure as Code security scanning
   - Compliance scanning (CIS benchmarks, PCI-DSS)
   - Security gate failure policies (block, warn, report)

6. ARTIFACT MANAGEMENT: Design artifact lifecycle:
   - Artifact format and naming conventions
   - Artifact repository selection (Nexus, Artifactory, ECR, GCR)
   - Artifact versioning strategy (semantic, build number, git SHA)
   - Artifact promotion workflow (dev → staging → prod)
   - Artifact retention and cleanup policies
   - Artifact signing and provenance (SLSA, SBOM)
   - Artifact attestation and verification
   - Container image management and registry strategy

7. DEPLOYMENT STRATEGY: Design deployment patterns:
   - Deployment target environment specifications
   - Deployment strategy selection (rolling, blue-green, canary)
   - Traffic shifting strategy (incremental, weight-based)
   - Database migration strategy and coordination
   - Feature flag integration for progressive rollout
   - Deployment window and maintenance scheduling
   - Multi-region deployment coordination
   - Deployment approval and change management

8. ROLLBACK AND RECOVERY: Design failure handling:
   - Automatic rollback triggers and criteria
   - Manual rollback procedures and runbooks
   - Database rollback strategy (forward-fix vs rollback)
   - Artifact rollback and previous version deployment
   - Configuration rollback and drift correction
   - Incident response integration
   - Post-deployment verification and smoke tests
   - Rollback testing and validation procedures

9. OBSERVABILITY AND MONITORING: Design pipeline observability:
   - Pipeline metrics (duration, success rate, MTTR)
   - Build and test result dashboards
   - Deployment frequency and lead time tracking
   - Error rate and failure analysis
   - Pipeline cost tracking and optimization
   - Developer experience metrics (feedback loop time)
   - Alerting for pipeline failures and degradation
   - Audit logging and compliance reporting

10. OPERATIONAL EXCELLENCE: Design for maintainability:
    - Pipeline documentation and runbooks
    - Pipeline template library and reuse
    - Developer onboarding for pipeline usage
    - Pipeline maintenance and upgrade schedule
    - Secret management and rotation
    - Runner/agent management and scaling
    - Pipeline performance optimization
    - Disaster recovery for pipeline infrastructure

Present the output as a structured CI/CD pipeline specification with stage diagrams (described textually), configuration examples, and operational runbook outlines for each major component.
```

## Example
### Original Prompt
```text
Set up a CI/CD pipeline for our Node.js application.
```

### Enhanced Prompt
```text
You are a senior DevOps engineer specializing in CI/CD pipeline architecture, deployment strategies, and developer experience optimization. Transform the following request into a structured CI/CD pipeline specification. Follow these steps precisely:

1. PIPELINE ARCHITECTURE: Design the overall pipeline structure:
   - Pipeline trigger strategy (push, PR, schedule, manual)
   - Pipeline stages and their purposes
   - Parallel vs sequential execution decisions
   - Pipeline templates and reusable components
   - Monorepo vs polyrepo pipeline strategy
   - Branch strategy and environment mapping
   - Pipeline as code organization and versioning
   - Cross-pipeline dependencies and orchestration

2. BUILD STAGE: Design the build process:
   - Source code checkout and dependency caching
   - Build environment selection (container, VM, runner)
   - Build matrix strategy (multiple languages, versions, OS)
   - Dependency management and lock file handling
   - Build artifact generation and packaging
   - Build time optimization (caching, parallelism, incremental)
   - Build reproducibility and hermetic builds
   - Build metadata and provenance tracking

3. TEST STAGE: Design the testing pipeline:
   - Test strategy pyramid (unit, integration, e2e)
   - Test execution ordering and prioritization
   - Test parallelization and sharding strategy
   - Test environment provisioning and teardown
   - Test data management and fixtures
   - Test coverage tracking and enforcement
   - Test result reporting and failure analysis
   - Flaky test detection and quarantine

4. QUALITY GATES: Design validation checkpoints:
   - Code quality gates (linting, formatting, complexity)
   - Test coverage thresholds and enforcement
   - Security scanning gates (SAST, DAST, SCA)
   - Dependency vulnerability scanning
   - License compliance checking
   - Performance testing gates (load, stress)
   - Accessibility testing gates (WCAG compliance)
   - Manual approval gates and sign-off requirements

5. SECURITY INTEGRATION: Embed security in the pipeline:
   - SAST (Static Application Security Testing) integration
   - DAST (Dynamic Application Security Testing) integration
   - SCA (Software Composition Analysis) for dependencies
   - Container image scanning and signing
   - Secret scanning and detection
   - Infrastructure as Code security scanning
   - Compliance scanning (CIS benchmarks, PCI-DSS)
   - Security gate failure policies (block, warn, report)

6. ARTIFACT MANAGEMENT: Design artifact lifecycle:
   - Artifact format and naming conventions
   - Artifact repository selection (Nexus, Artifactory, ECR, GCR)
   - Artifact versioning strategy (semantic, build number, git SHA)
   - Artifact promotion workflow (dev → staging → prod)
   - Artifact retention and cleanup policies
   - Artifact signing and provenance (SLSA, SBOM)
   - Artifact attestation and verification
   - Container image management and registry strategy

7. DEPLOYMENT STRATEGY: Design deployment patterns:
   - Deployment target environment specifications
   - Deployment strategy selection (rolling, blue-green, canary)
   - Traffic shifting strategy (incremental, weight-based)
   - Database migration strategy and coordination
   - Feature flag integration for progressive rollout
   - Deployment window and maintenance scheduling
   - Multi-region deployment coordination
   - Deployment approval and change management

8. ROLLBACK AND RECOVERY: Design failure handling:
   - Automatic rollback triggers and criteria
   - Manual rollback procedures and runbooks
   - Database rollback strategy (forward-fix vs rollback)
   - Artifact rollback and previous version deployment
   - Configuration rollback and drift correction
   - Incident response integration
   - Post-deployment verification and smoke tests
   - Rollback testing and validation procedures

9. OBSERVABILITY AND MONITORING: Design pipeline observability:
   - Pipeline metrics (duration, success rate, MTTR)
   - Build and test result dashboards
   - Deployment frequency and lead time tracking
   - Error rate and failure analysis
   - Pipeline cost tracking and optimization
   - Developer experience metrics (feedback loop time)
   - Alerting for pipeline failures and degradation
   - Audit logging and compliance reporting

10. OPERATIONAL EXCELLENCE: Design for maintainability:
    - Pipeline documentation and runbooks
    - Pipeline template library and reuse
    - Developer onboarding for pipeline usage
    - Pipeline maintenance and upgrade schedule
    - Secret management and rotation
    - Runner/agent management and scaling
    - Pipeline performance optimization
    - Disaster recovery for pipeline infrastructure

Set up a CI/CD pipeline for our Node.js application.

Present the output as a structured CI/CD pipeline specification with stage diagrams (described textually), configuration examples, and operational runbook outlines for each major component.
```

## Notes
- The quality gates section is where most pipelines fail — force explicit gate criteria
- Security integration should be shift-left, not bolted on at the end
- The rollback strategy is often the most critical section for production reliability
- For regulated environments, expand security and compliance scanning with specific framework requirements
- The observability section should track DORA metrics for engineering productivity

## Tags
`CI-CD` `pipeline` `GitHub-Actions` `GitLab-CI` `Jenkins` `ArgoCD` `deployment` `quality-gates` `security-scanning` `DevOps` `release-management` `GitOps`
