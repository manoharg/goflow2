# Comprehensive Design Document for NAT Option Template Support

## 1. Port-based Template Keying with AddrPort
This section describes how to implement port-based template keying using the AddrPort methodology to enhance the flexibility and efficiency of NAT option templates. Keying template data by both address and port allows for more granular control and better resource utilization.

## 2. Option Template Data Structure
The proposed data structure for option templates is designed to accommodate various NAT options and configurations. It includes:
- **Template ID:** Unique identifier for the template
- **Options:** A list of NAT options that can be configured
- **AddrPort:** Address and port mapping for keying.

## 3. TTL Configuration from CLI Flags
The Time To Live (TTL) for NAT templates can be configured through command-line interface (CLI) flags, enabling users to customize the expiration time for template entries. Suggested flags:
- `--ttl`: Default TTL value.
- `--ttl-custom`: Custom TTL value for specific templates.

## 4. Cleanup Strategy Using FlowStore
To ensure efficient memory management and avoid resource leaks, the cleanup strategy utilizes FlowStore to periodically remove inactive or stale NAT templates based on their TTL settings. This section will outline the strategy and frequency of cleanup operations.

## 5. Horizontal Scalability via Load Balancing
This section covers the implementation of horizontal scalability through load balancing across multiple instances of NAT option templates. Strategies for managing load and distributing traffic efficiently will be discussed.

## 6. Step-by-Step Implementation Guide with Code Examples
A detailed guide on how to implement NAT option template support step-by-step, including code snippets and examples that clearly illustrate each part of the process. This will help developers integrate the new functionality with ease.

---

This design document serves as a guideline for implementing NAT option template support in the Goflow2 repository and aims to enhance the current capabilities of the flow management system.