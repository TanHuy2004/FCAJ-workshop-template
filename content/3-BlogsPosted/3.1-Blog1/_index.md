---
title: "Blog 1"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---
{{% notice warning %}}
⚠️ **Note:** The information below is for reference purposes only. Please **do not copy verbatim** for your report, including this warning.
{{% /notice %}}

# Access control patterns for web applications on AWS with Amazon Cognito

## Introduction

When developing a web application, building only a login feature is not enough. More importantly, the system must ensure that only authenticated users can access its APIs and resources. Without a proper access control mechanism, APIs may be accessed without authorization, which can affect the security of the application.

Instead of building the entire authentication and authorization system from scratch, AWS provides several services that simplify this process. Amazon Cognito is one of the most common services for user management and supports modern authentication standards such as OAuth 2.0 and OpenID Connect.

After reviewing AWS documentation, I found that there are three common architecture patterns used to protect web applications. Each pattern has its own advantages and is suitable for different types of systems.

## How does OAuth 2.0 work?

The common point of all three patterns is that they use Amazon Cognito to authenticate users through OAuth 2.0.

The flow is quite simple:

* The user accesses the application.
* The system redirects the user to the Amazon Cognito login page.
* After a successful login, Cognito issues an Access Token or JWT.
* Requests sent to the backend include this token.
* The AWS service or backend validates the token before allowing access to resources.

As a result, the backend does not need to manage login sessions by itself. It only needs to trust the authentication result provided by Cognito.

## Pattern 1: Application Load Balancer with Amazon Cognito

This is a simple and easy-to-implement pattern for traditional web applications.

![Pattern 1: Application Load Balancer with Amazon Cognito](/FCAJ-workshop-template/images/3-BlogsPosted/blog1/model-1-alb-cognito.png)

In this pattern, the Application Load Balancer (ALB) handles user authentication. When a user accesses the application for the first time, the ALB automatically redirects the user to the Amazon Cognito login page. After the user logs in successfully, the ALB receives the authentication information from Cognito, creates a session cookie, and stores the login state.

For later requests, the ALB only needs to check the cookie before forwarding the request to the backend. This allows the backend to avoid handling login logic or token validation.

### Advantages

* The backend becomes simpler because it does not need to authenticate users by itself.
* It is easy to deploy for traditional web applications.
* It reduces the workload on the server.

### Limitations

* It depends on session cookies.
* It is not the best choice for API-based systems or mobile applications.

## Pattern 2: Amazon API Gateway with Amazon Cognito

If the application is built using REST APIs or a microservices architecture, API Gateway is usually a more suitable option.

![Pattern 2: Amazon API Gateway with Amazon Cognito](/FCAJ-workshop-template/images/3-BlogsPosted/blog1/model-2-api-gateway-cognito.png)

In this pattern, users log in with Amazon Cognito to receive an Access Token. Each time an API is called, the token is sent in the Authorization header. API Gateway validates the JWT before forwarding the request to the backend.

If the token is invalid or expired, the request is rejected directly at API Gateway and does not reach the backend system.

### Advantages

* Suitable for REST APIs and HTTP APIs.
* Supports direct JWT authentication.
* Reduces the load on the backend.
* Easier to scale when the system grows using a microservices architecture.

### Limitations

* The user or client application needs to manage the Access Token.
* The initial configuration may be more complex than the ALB pattern.

## Pattern 3: CloudFront with Lambda@Edge

This pattern provides a higher security level and is often used when the application serves users across multiple regions.

![Pattern 3: CloudFront with Lambda@Edge](/FCAJ-workshop-template/images/3-BlogsPosted/blog1/model-3-cloudfront-lambda-edge.png)

CloudFront receives the first request from the user. Before the request is forwarded to the backend, Lambda@Edge is triggered to validate the Access Token.

If the token is valid, CloudFront continues forwarding the request to the Application Load Balancer. In addition, CloudFront can add a custom header so that the ALB knows the request actually came through CloudFront. This helps prevent direct access to the backend.

### Advantages

* Improves security.
* Validates requests at the Edge Location.
* Combines access control with CloudFront acceleration.

### Limitations

* More complex to implement.
* Lambda@Edge must be deployed in the us-east-1 Region.
* Cost and operational management are higher than the other two patterns.

## Comparing the three patterns

If the application is a normal website, Application Load Balancer with Amazon Cognito is the simplest and easiest option to implement.

For systems that provide APIs for web or mobile applications, API Gateway is more suitable because it can validate JWTs directly and integrates well with microservices architectures.

Meanwhile, CloudFront with Lambda@Edge is suitable for larger systems that need both performance optimization and stronger security while serving users globally.

## Conclusion

After learning about these three patterns, I found that AWS provides enough managed solutions to solve authentication and access control problems without requiring developers to build the entire security system from scratch.

Depending on the scale and architecture of the application, we can choose ALB, API Gateway, or CloudFront with Lambda@Edge to meet real-world requirements. Using AWS managed services not only reduces development effort but also improves security, scalability, and system stability.

**References**

* AWS Architecture Blog: *Access control patterns for web applications using AWS services*.
* Amazon Cognito documentation.
* Application Load Balancer authentication documentation.
* Amazon API Gateway JWT authorizer documentation.
