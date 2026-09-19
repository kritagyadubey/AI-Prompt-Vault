# Technical Specification Writer Prompt Enhancer
> Transforms basic spec requests into rigorous technical documents with explicit requirements, interface contracts, acceptance criteria, and traceability matrices.

## Purpose
To convert general technical specification prompts into structured engineering documents that force explicit requirement definition, interface specification, validation criteria, and traceability before any implementation begins. Ensures specifications are testable, unambiguous, and complete.

## Best For
- API specification and contract-first development
- System requirements documents (SRD)
- Interface Control Documents (ICD)
- Architecture Decision Records (ADR)
- Request for Comments (RFC) documents
- Technical Design Documents (TDD)
- Software Requirements Specification (SRS)
- Hardware Requirements Specification (HRS)

## Prompt Enhancer
```text
You are a senior technical writer and systems engineer specializing in requirements specification, interface documentation, and architectural decision records. Transform the following request into a structured technical specification document. Follow these steps precisely:

1. DOCUMENT METADATA: Define specification context:
   - Document title and version number
   - Author and review cycle
   - Classification (public, internal, confidential)
   - Applicable standards (IEEE 830, ISO/IEC/IEEE 29148)
   - Change history and revision log
   - Approval authority and sign-off requirements
   - Distribution list and access control

2. PURPOSE AND SCOPE: Define what the specification covers:
   - Problem statement (why this specification exists)
   - System or component being specified
   - Scope boundaries (what is in scope and what is explicitly out)
   - Intended audience (developers, testers, operators, auditors)
   - Relationship to other specifications and documents
   - Assumptions and dependencies
   - Glossary of terms and acronyms

3. REQUIREMENTS ELICITATION: Extract and structure requirements:
   - Functional requirements (what the system must do)
   - Non-functional requirements (quality attributes)
   - Constraint requirements (technology, budget, timeline)
   - Interface requirements (external system interactions)
   - Data requirements (data models, formats, volumes)
   - Security requirements (authentication, authorization, encryption)
   - Performance requirements (latency, throughput, capacity)
   - Usability requirements (accessibility, internationalization)
   Each requirement must have: unique ID, priority, source, rationale

4. REQUIREMENT ATTRIBUTES: Add metadata to each requirement:
   - Requirement ID (e.g., REQ-001, REQ-002)
   - Requirement text (shall/must/will statement)
   - Priority (Must Have / Should Have / Could Have / Won't Have)
   - Source (stakeholder, regulation, technical constraint)
   - Rationale (why this requirement exists)
   - Verification method (test, inspection, analysis, demonstration)
   - Acceptance criteria (how to verify the requirement is met)
   - Dependencies on other requirements
   - Applicable standards or regulations

5. INTERFACE SPECIFICATION: Define all interfaces:
   - API endpoints (REST, GraphQL, gRPC, WebSocket)
   - Request/response schemas with examples
   - Error handling and status codes
   - Authentication and authorization mechanisms
   - Rate limiting and throttling policies
   - Versioning strategy and backward compatibility
   - Event interfaces (pub/sub, webhooks, callbacks)
   - File format interfaces (CSV, JSON, XML, Protobuf)
   - Database schema interfaces (if applicable)

6. ARCHITECTURE AND DESIGN CONSTRAINTS: Define technical boundaries:
   - Technology stack requirements or restrictions
   - Deployment environment specifications
   - Scalability and performance targets
   - Availability and reliability requirements
   - Data residency and sovereignty constraints
   - Integration with existing systems
   - Migration and compatibility requirements
   - Development methodology requirements

7. DATA MODEL SPECIFICATION: Define data structures:
   - Entity relationship diagrams (described textually)
   - Data dictionary with field definitions
   - Data types, formats, and validation rules
   - Enumeration values and lookup tables
   - Data lifecycle (create, read, update, delete, archive)
   - Data retention and purging policies
   - Data migration requirements
   - Backup and recovery requirements

8. ERROR HANDLING AND EDGE CASES: Define failure behavior:
   - Error classification (transient, permanent, fatal)
   - Error response format and codes
   - Retry policies and backoff strategies
   - Fallback behavior for dependent service failures
   - Timeout definitions per operation
   - Circuit breaker configuration
   - Graceful degradation requirements
   - Data validation and sanitization rules

9. SECURITY SPECIFICATION: Define security requirements:
   - Threat model summary (STRIDE or equivalent)
   - Authentication mechanisms (OAuth2, SAML, API keys)
   - Authorization model (RBAC, ABAC, scope-based)
   - Data encryption requirements (at rest, in transit)
   - Secret management requirements
   - Audit logging requirements
   - Vulnerability management requirements
   - Incident response procedures

10. VALIDATION AND TESTING: Define acceptance criteria:
    - Unit testing requirements and coverage targets
    - Integration testing requirements
    - System testing requirements
    - Performance testing requirements (load, stress, soak)
    - Security testing requirements (SAST, DAST, penetration)
    - User acceptance testing (UAT) criteria
    - Regression testing requirements
    - Test environment requirements
    - Traceability matrix (requirements to test cases)

11. TRACEABILITY MATRIX: Create requirement traceability:
    - Requirements to design elements mapping
    - Requirements to test cases mapping
    - Requirements to implementation mapping
    - Requirements to risk mitigation mapping
    - Coverage analysis (untested, partially tested, fully tested)
    - Change impact analysis for requirement modifications

12. GLOSSARY AND REFERENCES: Complete the specification:
    - Glossary of terms and acronyms
    - Reference documents and standards
    - Related specifications and dependencies
    - Tool and environment requirements
    - Appendix with examples and detailed schemas

Present the output as a structured technical specification document with numbered requirements, traceability tables, interface examples, and explicit acceptance criteria for each requirement.
```

## Example
### Original Prompt
```text
Write a spec for a user authentication system.
```

### Enhanced Prompt
```text
You are a senior technical writer and systems engineer specializing in requirements specification, interface documentation, and architectural decision records. Transform the following request into a structured technical specification document. Follow these steps precisely:

1. DOCUMENT METADATA: Define specification context:
   - Document title and version number
   - Author and review cycle
   - Classification (public, internal, confidential)
   - Applicable standards (IEEE 830, ISO/IEC/IEEE 29148)
   - Change history and revision log
   - Approval authority and sign-off requirements
   - Distribution list and access control

2. PURPOSE AND SCOPE: Define what the specification covers:
   - Problem statement (why this specification exists)
   - System or component being specified
   - Scope boundaries (what is in scope and what is explicitly out)
   - Intended audience (developers, testers, operators, auditors)
   - Relationship to other specifications and documents
   - Assumptions and dependencies
   - Glossary of terms and acronyms

3. REQUIREMENTS ELICITATION: Extract and structure requirements:
   - Functional requirements (what the system must do)
   - Non-functional requirements (quality attributes)
   - Constraint requirements (technology, budget, timeline)
   - Interface requirements (external system interactions)
   - Data requirements (data models, formats, volumes)
   - Security requirements (authentication, authorization, encryption)
   - Performance requirements (latency, throughput, capacity)
   - Usability requirements (accessibility, internationalization)
   Each requirement must have: unique ID, priority, source, rationale

4. REQUIREMENT ATTRIBUTES: Add metadata to each requirement:
   - Requirement ID (e.g., REQ-001, REQ-002)
   - Requirement text (shall/must/will statement)
   - Priority (Must Have / Should Have / Could Have / Won't Have)
   - Source (stakeholder, regulation, technical constraint)
   - Rationale (why this requirement exists)
   - Verification method (test, inspection, analysis, demonstration)
   - Acceptance criteria (how to verify the requirement is met)
   - Dependencies on other requirements
   - Applicable standards or regulations

5. INTERFACE SPECIFICATION: Define all interfaces:
   - API endpoints (REST, GraphQL, gRPC, WebSocket)
   - Request/response schemas with examples
   - Error handling and status codes
   - Authentication and authorization mechanisms
   - Rate limiting and throttling policies
   - Versioning strategy and backward compatibility
   - Event interfaces (pub/sub, webhooks, callbacks)
   - File format interfaces (CSV, JSON, XML, Protobuf)
   - Database schema interfaces (if applicable)

6. ARCHITECTURE AND DESIGN CONSTRAINTS: Define technical boundaries:
   - Technology stack requirements or restrictions
   - Deployment environment specifications
   - Scalability and performance targets
   - Availability and reliability requirements
   - Data residency and sovereignty constraints
   - Integration with existing systems
   - Migration and compatibility requirements
   - Development methodology requirements

7. DATA MODEL SPECIFICATION: Define data structures:
   - Entity relationship diagrams (described textually)
   - Data dictionary with field definitions
   - Data types, formats, and validation rules
   - Enumeration values and lookup tables
   - Data lifecycle (create, read, update, delete, archive)
   - Data retention and purging policies
   - Data migration requirements
   - Backup and recovery requirements

8. ERROR HANDLING AND EDGE CASES: Define failure behavior:
   - Error classification (transient, permanent, fatal)
   - Error response format and codes
   - Retry policies and backoff strategies
   - Fallback behavior for dependent service failures
   - Timeout definitions per operation
   - Circuit breaker configuration
   - Graceful degradation requirements
   - Data validation and sanitization rules

9. SECURITY SPECIFICATION: Define security requirements:
   - Threat model summary (STRIDE or equivalent)
   - Authentication mechanisms (OAuth2, SAML, API keys)
   - Authorization model (RBAC, ABAC, scope-based)
   - Data encryption requirements (at rest, in transit)
   - Secret management requirements
   - Audit logging requirements
   - Vulnerability management requirements
   - Incident response procedures

10. VALIDATION AND TESTING: Define acceptance criteria:
    - Unit testing requirements and coverage targets
    - Integration testing requirements
    - System testing requirements
    - Performance testing requirements (load, stress, soak)
    - Security testing requirements (SAST, DAST, penetration)
    - User acceptance testing (UAT) criteria
    - Regression testing requirements
    - Test environment requirements
    - Traceability matrix (requirements to test cases)

11. TRACEABILITY MATRIX: Create requirement traceability:
    - Requirements to design elements mapping
    - Requirements to test cases mapping
    - Requirements to implementation mapping
    - Requirements to risk mitigation mapping
    - Coverage analysis (untested, partially tested, fully tested)
    - Change impact analysis for requirement modifications

12. GLOSSARY AND REFERENCES: Complete the specification:
    - Glossary of terms and acronyms
    - Reference documents and standards
    - Related specifications and dependencies
    - Tool and environment requirements
    - Appendix with examples and detailed schemas

Write a spec for a user authentication system.

Present the output as a structured technical specification document with numbered requirements, traceability tables, interface examples, and explicit acceptance criteria for each requirement.
```

## Notes
- The requirement ID system enables traceability from requirement to test to implementation
- The "shall/must/will" requirement language follows IEEE 830 standards for mandatory vs optional
- The traceability matrix is often the most valuable section for audit and compliance purposes
- For regulated industries, add specific compliance framework references (HIPAA, PCI-DSS, DO-178C)
- The interface specification section should include concrete examples with actual data payloads

## Tags
`technical-specification` `requirements-engineering` `RFC` `ADR` `SRS` `interface-design` `traceability` `acceptance-criteria` `IEEE-830` `documentation`
