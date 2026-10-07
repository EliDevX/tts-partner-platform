# TTS Partner Platform

> An early-stage full-stack platform for productizing cross-border e-commerce services.

[![Next.js](https://img.shields.io/badge/Next.js-black?logo=next.js)](https://nextjs.org/) [![TypeScript](https://img.shields.io/badge/TypeScript-blue?logo=typescript)](https://www.typescriptlang.org/) [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white)](https://www.postgresql.org/) [![Prisma](https://img.shields.io/badge/Prisma-2D3748?logo=prisma&logoColor=white)](https://www.prisma.io/) [![Vercel](https://img.shields.io/badge/Vercel-black?logo=vercel&logoColor=white)](https://vercel.com/)

## Overview

TTS Partner Platform is an early-stage full-stack web application that I designed and developed around a real cross-border e-commerce service business.

The original goal was to explore whether a traditionally manual service business could be transformed into a structured digital platform. The platform was designed to let customers discover services, submit requirements, create orders, make payments, and eventually manage service delivery through a web application.

This was not built as a purely academic or tutorial project. I used the actual business workflow as the basis for the product design, allowing me to evaluate both the engineering challenges and the product assumptions behind the system.

The original product model was:

**External Traffic → Website → Service Discovery → Customer Requirement → Order → Payment → Service Delivery**

The platform also explored a private-domain customer conversion workflow:

**External Traffic → Website → Customer Requirement → Private-domain Contact → Consultation → Conversion → Service Delivery**

The difference between these two workflows eventually became the key reason why the project was paused.

## Product & Engineering

The project was designed as a full-stack application with a clear separation between the presentation, application, authentication, and data layers.

**Application flow**

```text
Client
  ↓
Next.js / React / TypeScript
  ↓
Application & Business Logic
  ↓
Better Auth
  ↓
Prisma ORM
  ↓
PostgreSQL
```

I designed the overall application architecture and made the major technology decisions myself.

| Area | Technology |
| --- | --- |
| Framework | Next.js |
| Language | TypeScript |
| UI | React, Tailwind CSS, shadcn/ui |
| Authentication | Better Auth |
| ORM | Prisma |
| Database | PostgreSQL |
| Deployment | Vercel |

I chose Next.js partly because I was learning the framework when I started this project. Instead of learning it only through isolated tutorials, I used a real application to explore full-stack routing, application architecture, authentication, database integration, reusable components, and deployment.

The database was integrated with PostgreSQL through Prisma, providing the foundation for customer, service, and order-related data.

The interface was built with React, Tailwind CSS, and shadcn/ui, with an emphasis on reusable components and a consistent application structure.

## Implementation

The project reached an early functional prototype.

The implemented foundation included:

- Responsive service-oriented web interface
- Service presentation and information architecture
- Customer onboarding flow
- Customer information collection
- Authentication
- PostgreSQL database integration
- Prisma ORM integration
- Initial service and order data structures
- Private-domain customer conversion flow
- Reusable UI components
- Production deployment through Vercel

The following parts were planned but not completed:

- Complete customer-side order management
- Complete administrator dashboard
- Full order lifecycle management
- Production payment integration
- Complete service delivery workflow

The database and core application architecture were already established when the project was paused.

## Development Approach

The overall engineering structure, product architecture, database approach, technology selection, and implementation direction were designed by me.

I also used AI-assisted development tools throughout the project. AI was used as a development collaborator for implementation, debugging, refactoring, code generation, and coordinating repetitive development tasks.

The use of AI did not replace the architectural or product decisions. I remained responsible for defining the system requirements, designing the architecture, selecting technologies, evaluating implementations, and deciding which direction the product should take.

This project was also an important part of my transition from learning frameworks to building complete applications. I was learning Next.js at the time, so I deliberately used the project as a practical environment to understand how a modern full-stack application is structured and deployed.

## Product Evolution

The most important part of this project was the change in the product hypothesis.

The original assumption was that cross-border e-commerce services could be packaged similarly to traditional e-commerce products:

**Service → Fixed Offering → Fixed Price → Online Checkout → Automated Order**

After operating the actual business and testing the platform against real business scenarios, I found that this assumption was only partially correct.

Many services require consultation before delivery. Customer requirements vary, pricing and availability can change with platform policies, and service delivery often requires human evaluation and execution.

This created several limitations for a fully transactional model:

1. **Customer requirements are not always standardized.** Different sellers can require different solutions depending on their products, stores, and operating conditions.

2. **Pricing and service availability can change quickly.** Cross-border e-commerce platforms frequently update policies and requirements, making rigid service packages difficult to maintain.

3. **Human involvement remains important.** Some services require communication, evaluation, and manual execution before the correct solution can be determined.

4. **The website does not necessarily need to be the final transaction layer.** Through real-world testing, I found that the website could be more effective as a customer-acquisition and trust-building layer, while consultation and conversion could happen through a private-domain relationship.

The product model therefore evolved from:

**Website → Payment → Service Delivery**

toward:

**Traffic → Website → Customer Requirement → Private-domain Contact → Consultation → Conversion → Human Delivery**

This was a significant change in my understanding of the role of software in a service business.

## Real-World Validation

The project was not officially launched as a public production service.

However, I developed and evaluated it using real scenarios from the cross-border e-commerce service business I was operating.

This allowed me to evaluate the platform from two perspectives.

From an engineering perspective, I explored how customers, services, authentication, data, and future order workflows could be represented in a full-stack system.

From a product perspective, I tested whether the proposed workflow actually matched customer behavior and the operational reality of a service business.

The second perspective ultimately changed the direction of the project.

This led to an important principle in my approach to software development:

> **Software should adapt to validated workflows rather than forcing real-world operations into a predetermined product model.**

## Engineering & Product Lessons

This project taught me that building software for a real business is different from building a technical demonstration.

A technically reasonable architecture can still be built around the wrong product assumption.

The original system could have been completed technically, but completing the remaining order, payment, and administration features would have meant investing more time into a transactional model that I no longer believed was the best fit for the business.

The experience changed the way I think about product development:

**Real-world Problem → Product Hypothesis → Software Implementation → Real-world Testing → Observation → Re-evaluation → Product Iteration**

The important lesson was not simply that the first idea was wrong. It was that a product should be allowed to change when evidence shows that the original assumption does not match reality.

I also learned that not every service should immediately be turned into a self-service product. The first step is to identify which parts of a workflow are repeatable and standardizable, and only then determine which parts are suitable for automation.

Stopping a project can therefore be a product decision rather than a failure to finish it. In this case, preserving the existing implementation while moving toward a better product model was more valuable than completing features based on outdated assumptions.

## Project Status

**Archived — Superseded by a new product direction**

This repository is no longer under active development.

The project was intentionally paused after the business model evolved. Instead of completing the remaining features around an outdated transactional assumption, I decided to preserve this implementation as an earlier product iteration and use what I learned to guide a new project.

The repository therefore represents a real stage in my development process:

**Business Problem → Product Hypothesis → Architecture → Implementation → Real-world Testing → Product Re-evaluation → New Direction**

The unfinished parts of the project are intentionally documented rather than hidden.

## Future Direction

The experience from this project has influenced the direction of my future work under **AsyncSoft**.

Instead of starting with a large transactional platform, I am now more interested in identifying repeated problems within cross-border e-commerce and turning validated workflows into focused software products.

The direction is:

**Real Customer Problem → Repeated Workflow → Standardization → Automation → Software Tool → SaaS**

The long-term goal is to combine practical business experience with software engineering to build tools and products that solve specific operational problems in cross-border e-commerce.

## Author

**Elijah Zheng**  
Founder & Developer at AsyncSoft

Full-stack development · Product engineering · Entrepreneurship · SaaS · Cross-border e-commerce technology
