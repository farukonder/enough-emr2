---
title: Containers
weight: 2
layout: post
date: '23.08.19'
---

Architecture Overview
----------------------

Tracers live in your applications and record timing and metadata about
operations that took place. They often instrument libraries, so that their use
is transparent to users. For example, an instrumented web server records when it
received a request and when it sent a response. The trace data collected is
called a Span.

Instrumentation is written to be safe in production and have little overhead.
For this reason, they only propagate IDs in-band, to tell the receiver there’s
a trace in progress. Completed spans are reported to Zipkin out-of-band,
similar to how applications report metrics asynchronously.

For example, when an operation is being traced and it needs to make an outgoing
http request, a few headers are added to propagate IDs. Headers are not used to
send details such as the operation name.
