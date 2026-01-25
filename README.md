# rproxy

A simple TCP proxy written in Rust for educational purposes.

## Overview

`rproxy` is a learning project created to explore low-level network programming, asynchronous I/O with Tokio, and systems design principles in Rust.

It is designed to listen for TCP connections on one address and forward all traffic to a pre-configured upstream destination.

## Status

This project is for learning and demonstration purposes. The initial goal is to implement a basic, concurrent TCP forwarder. See [DESIGN](/DESIGN.md) for more details on the architecture and roadmap.

## Usage

To build and run the project:

`cargo run`

_Note: The listener and upstream addresses are currently hardcoded in the source code._
