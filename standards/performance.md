# Performance Standard

## General
Measure before optimizing when possible. Identify the bottleneck and user/operational impact. Optimize critical paths first. Treat CPU, memory, network, database, startup, and perceived latency as distinct dimensions.

## Frontend
Minimize unnecessary JavaScript and render work. Optimize critical images/fonts and request waterfalls. Prevent layout shifts and long main-thread tasks. Use browser performance tools and Core Web Vitals where applicable.

## Backend
Set timeouts and resource bounds. Avoid blocking event loops and unbounded concurrency. Cache only with explicit freshness, invalidation, and memory policies. Measure query plans and connection-pool behavior. Apply pagination and backpressure.

## Operations
Monitor latency percentiles, throughput, error rates, saturation, and resource use. Establish baselines before capacity changes. Load-test realistic workloads and failure conditions. Never trade correctness, security, or data integrity for an unmeasured speed gain.
