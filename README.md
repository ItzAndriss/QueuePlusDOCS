# Introduction

QueuePlus is a modern, full-featured queue management plugin built for **Velocity** proxy networks.\
It ensures smooth server transitions, prevents player spam during restarts, and manages advanced features like developer mode, priority queueing, and lobby load balancing.

***

## Why QueuePlus?

Unlike basic queue plugins, QueuePlus provides:

* Real-time ActionBar feedback for queued players
* Automatic requeue after server restarts
* LuckPerms-based priority handling
* Developer-only access control (dev mode)
* Configurable delay after restarts (e.g., 30s warmup)
* Load-balanced multi-lobby routing
* Fully customizable messages via `config.toml`

***

## Overview

| Feature           | Description                                         |
| ----------------- | --------------------------------------------------- |
| Smart Requeue     | Automatically re-adds players after server restarts |
| Developer Mode    | Restrict access during maintenance or testing       |
| Priority Queue    | LuckPerms integration for ranked queue access       |
| Lobby Balancer    | Sends players to the least populated lobby          |
| ActionBar Updates | Live feedback showing queue position and status     |
| Configurable      | Every message and timing is editable                |

QueuePlus is designed to be production-ready for large-scale networks with minimal setup.
