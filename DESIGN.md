# rproxy - Design Document

**Author:** Uladzislau Blok
**Date:** 25.01.2026
**Status:** In Progress

## Motivation & Goals

**What is this?** A simple, single-threaded TCP proxy implemented in Rust as a learning project.
**Why build it?** To gain practical experience with Rust, low-level network I/O (sockets), and concurrent programming with Tokio.
**High-Level Goal:** To create a minimal, working TCP proxy that can forward traffic from a source address to a single destination address.

## Scope & Features (Phase 1)

#### In Scope:

- Listen for TCP connections on a hardcoded local address.
- For each incoming connection, establish a new connection to a hardcoded upstream server.
- Forward all data bidirectionally between the client and the upstream server.
- Handle multiple client connections concurrently using Tokio tasks.
- Log basic events (e.g., new connection, connection terminated) to the console.

#### Out of Scope (for now):

- Layer (HTTP) parsing.
- Load balancing across multiple upstream servers.
- Reading configuration from a file.
- TLS (HTTPS) support.
- Caching, retries, or other advanced features.

## High-Level Design

This is the "boxes and arrows" part of your plan.

## The Roadmap (Future Phases)

This turns your project into a journey.

-**Phase : Load Balancing:** Evolve the single upstream address into a list of addresses. Implement a simple round-robin strategy to select an upstream for each new connection.
_ **Phase : Configuration:** Remove hardcoded addresses and move them into a configuration file (e.g., `config.toml`).
_ **Phase : Layer Routing:** Inspect the initial bytes of a connection to make routing decisions (e.g., read the HTTP `Host` header).
