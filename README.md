# RUSTY-REDIS

Rusty-Redis is a learning-focused reimplementation of the Redis in-memory data structure store, built entirely in Rust. This project aims to explore and demonstrate the internals of Redis while leveraging Rust's powerful features for safety and concurrency.

# Features

1. Full reimplementation of Redis in Rust.
2. Support for core Redis data structures: strings, lists, sets, hashes, and sorted sets.
3. Learning-focused codebase with clear and concise implementations.
4. Basic networking for handling client connections and message encoding/decoding.
5. Simple persistence mechanisms for learning purposes.
6. Examples and documentation to aid in understanding Redis and Rust.


# Rusty-Redis Modules

## Server
- Handles startup, shutdown, and main event loop.
- Manages client connections and command processing.

## Networking
- Manages TCP connections.
- Implements RESP for message encoding/decoding.

## Data Structures
- Implements core data structures: strings, lists, sets, hashes, sorted sets.

## Commands
- Implements logic for Redis commands (e.g., `GET`, `SET`, `LPUSH`, `SADD`).
- Maps commands to data structure operations.

## Storage
- Manages data persistence (RDB snapshots, AOF).
- Handles saving/loading data to/from disk.

## Pub/Sub
- Implements publish/subscribe system.
- Manages channels and message distribution.

## Transactions
- Supports Redis transactions with `MULTI/EXEC`.
- Ensures atomic command execution.

## Scripting
- Provides Lua scripting support.
- Handles script execution and integration.

## Logging and Metrics
- Implements logging for events, errors, and commands.
- Collects server performance metrics.

## Configuration
- Manages server configuration options.
- Loads and validates configurations.

## Utilities
- Provides utility functions and helpers.
- Includes error handling, data encoding/decoding.



# Folder Structure


```plaintext
rusty-redis/
├── src/
│   ├── main.rs                  // Entry point of the application
│   ├── server.rs                // Server management
│   ├── networking.rs            // Networking module
│   ├── data_structures/         // Core data structures
│   │   ├── strings.rs
│   │   ├── lists.rs
│   │   ├── sets.rs
│   │   ├── hashes.rs
│   │   └── sorted_sets.rs
│   ├── commands.rs              // Command handling
│   ├── storage.rs               // Persistence mechanisms
│   ├── pubsub.rs                // Pub/Sub system
│   ├── transactions.rs          // Transaction support
│   ├── scripting.rs             // Lua scripting
│   ├── logging.rs               // Logging and metrics
│   ├── configuration.rs         // Configuration management
│   └── utils.rs                 // Utility functions and helpers
├── Cargo.toml                   // Project dependencies and metadata
└── README.md                    // Project description and documentation

```