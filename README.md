# ShetabPy

**An AOT-first, full-stack Python framework built for performance, developer experience, and deployment independence.**

ShetabPy is an open-source Python framework by Desi Script, inspired by the developer experience of [Shetab](https://www.desiscript.com/) and the build-time augmentation philosophy of frameworks like [Quarkus](https://quarkus.io/).

It brings Ahead-of-Time (AOT) application processing, decorator-driven development, compile-time dependency injection, and first-class React and TypeScript integration into a unified development experience.

ShetabPy is built around a simple philosophy:

**Do more at build time. Keep runtime lean. Scale without rewriting.**

## Vision

Traditional application frameworks perform significant work at runtime, repeatedly resolving metadata, dependencies, routes, and application configuration.

ShetabPy aims to shift as much of this work as possible to build time.

By analyzing application structure and preparing the execution environment ahead of time, ShetabPy seeks to minimize runtime overhead while providing a productive, expressive development experience.

But performance is only one part of the vision.

An application should not be tied to a particular server, process model, or deployment infrastructure. Developers should be able to start with a single VPS and grow into distributed infrastructure and Kubernetes without rewriting their application.

## Core Architectural Principles

### 1. Ahead-of-Time First

Application processing should happen at build time wherever possible.

- AOT application compilation and optimization
- Precomputed route registration and metadata
- Compile-time dependency graph construction
- Reduced runtime reflection and discovery
- Optimized request handling and serialization

The goal is predictable runtime behavior with minimal unnecessary overhead.

### 2. Decorator-Driven Development

Python decorators provide an expressive way to define application behavior.

ShetabPy aims to use decorators for:

- HTTP route definitions
- Controller configuration
- Dependency injection
- Middleware registration
- Application configuration
- Request handling and validation

The framework combines Python's expressive syntax with build-time processing rather than relying on expensive runtime discovery.

### 3. Compile-Time Dependency Injection

Dependency injection should be predictable, explicit, and optimized before application execution.

ShetabPy aims to provide:

- Compile-time dependency resolution
- Interface-oriented dependency wiring
- Defined dependency lifetimes
- Application-scoped dependencies
- Request-scoped dependencies
- Transient dependencies
- Reduced runtime container overhead

The objective is to make dependency management convenient without sacrificing execution efficiency.

### 4. Dual Execution Model

Different deployment environments have different execution requirements.

ShetabPy envisions two complementary execution models using the same application programming model.

**Cold-Start Execution**

Designed for request-isolated environments where an application process can be initialized for an individual request.

Potential use cases include CGI-style hosting and environments where process isolation is desirable.

**Persistent Worker Execution**

Designed for long-running application processes that initialize the application once and handle multiple requests.

Potential benefits include:

- Reusing initialized application resources
- Persistent dependency containers
- Database connection pooling
- Reduced application bootstrap overhead
- Efficient asynchronous request handling

Developers should be able to switch between execution models without modifying application business logic.

### 5. Deployment Independence

Application architecture should remain independent of deployment infrastructure.

ShetabPy aims to support an evolutionary deployment path:

| Environment | Deployment model |
|---|---|
| Standalone | Single VPS |
| Multi-process | Multiple application workers |
| Distributed | Multiple application servers |
| Containerized | Docker deployments |
| Orchestrated | Kubernetes deployments |

The long-term objective is to make deployment behavior configurable through environment variables and deployment configuration rather than application-code changes.

Developers should be able to scale their infrastructure as their applications grow without redesigning their applications.

### 6. Full-Stack React Integration

ShetabPy aims to provide a unified development experience for Python and React.

Planned and targeted capabilities include:

- First-class React integration
- Server-Side Rendering (SSR)
- Static Site Generation (SSG)
- Incremental Static Regeneration (ISR)
- Client-side hydration
- TypeScript integration
- Automatic TypeScript type generation

The goal is to bridge the Python backend and modern frontend development without introducing unnecessary architectural complexity.

## Developer Experience

ShetabPy is designed to make application development expressive without making runtime execution dependent on expensive dynamic abstractions.

The intended developer experience combines:

- Python decorators for application definitions
- Build-time application analysis
- Predictable dependency injection
- Unified backend and frontend development
- Environment-driven configuration
- Consistent development and production workflows

## Runtime Philosophy

ShetabPy distinguishes application logic from application execution.

The same application should be capable of running under different execution models and deployment environments.

The framework aims to manage the underlying concerns:

- Application initialization
- Worker lifecycle
- Request lifecycle
- Dependency lifecycle
- Concurrency
- Graceful shutdown
- Health and readiness checks
- Resource management

Infrastructure-specific responsibilities, such as container orchestration, load balancing, and replica scheduling, should integrate with the runtime rather than become application-level concerns.

## Technology Direction

ShetabPy is built around the Python ecosystem while drawing inspiration from modern build-time-oriented frameworks.

Its architectural direction includes:

- Python for application development
- Decorators for declarative configuration
- AOT processing for build-time optimization
- React for frontend development
- TypeScript for frontend type safety
- ASGI-oriented request handling
- Container-friendly deployment architecture

## Project Philosophy

ShetabPy follows a few fundamental principles:

1. **Build-time over runtime:** Resolve as much as possible before application execution.
2. **Performance without complexity:** Avoid unnecessary runtime abstractions.
3. **Developer experience matters:** Powerful architecture should remain approachable.
4. **Deployment should be evolutionary:** Start small, scale progressively.
5. **Application code should be portable:** Infrastructure changes should not require business logic rewrites.
6. **One application, multiple execution models:** Execution strategy should not dictate application architecture.

## About

ShetabPy is an open-source project by **Desi Script**, exploring a different approach to Python application architecture.

It draws inspiration from Shetab's AOT philosophy and modern frameworks such as Quarkus, while pursuing its own approach to Python development and execution.

**ShetabPy — Python development, reimagined around AOT.**

---

*Note: This README describes the project's architectural direction and intended capabilities. Individual features and execution modes should be considered experimental or planned until implemented and documented.*
