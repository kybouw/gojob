# gojob

Distributed task scheduler built with Rust + Go.

## Status

🚧 **Proof of Concept** - Currently implementing basic controller/worker communication.

## Architecture

- **Controller** (Go): Job queue, scheduling, API
- **Worker** (Rust): Sandboxed job execution

## Roadmap

- [x] Project setup
- [ ] PoC: In-memory queue + single worker
- [ ] PostgreSQL integration
- [ ] Cron scheduling
- [ ] Retry logic with exponential backoff
- [ ] Job dependencies
- [ ] Resource limits & sandboxing
- [ ] Web dashboard

## Quick Start

**Run PoC:**

```bash
# Terminal 1: Start controller
$ cd controller
$ go run cmd/controller/main.go

# Terminal 2: Start worker
$ cd worker
$ cargo run -- --controller http://localhost:8080
```

## Why This Exists

I wanted to explore Rust and Go, and I was already familiar with building a task
scheduling service. So I could immediately see the impact of such a thing.

## Inspiration

- Advanced Python Scheduler

## License

Copyright 2026 Kyle Bouwman

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
