[![Actions Status](https://github.com/project-legion/legion/workflows/unit-tests/badge.svg)](https://github.com/project-legion/actions)
[![Actions Status](https://github.com/project-legion/legion/workflows/checks/badge.svg)](https://github.com/project-legion/actions)

# Legion

## Goals
 * Scaleable to billions or trillions of nodes
 * Runtime agnaustic orchestrator, will support OCI initially.
 * Control-plane vs worker node == no difference for install/user.
 * Single binary install
 * Based on promise theory?
 * HA on as few as 3 nodes
 * Gitops core?

## Non-goals
 * Service mesh
 * Other things 

## Project pre-alpha road map 
 - [x] Initial Cluster API
 - [x] Node to node cluster communication interface
 - [x] Node to node cluster communication implementation (zeroMQ)
 - [x] Container Runtime integration
 - [ ] Resource Defs
 - [ ] Git Mech
 - [ ] Machine taints

## Building and testing
Building and local unit testing are made simple by cargo.

### Building

#### requirements
Requires both cmake and protocal buffers installed. Want to help out with this project? add more instructions here :)

#### building

`cargo build`
use the `--release` flag for a more optimized build. It will take longer to compile.

### Testing
`cargo check && cargo fmt -- --check && cargo clippy`

It could be required for you to use `rustup component add clippy && rustup component add fmt` to use those commands.

Currently there are a few failures in check and clippy; in the future both of these will be required 
to pass to all of these to be merged.

## Tech Stack Overview
 * [ClusterAPI](docs/cluster_api.md) app 
 * [Node Communication Interface](docs/nci.md)
 * [Node Communication implementation](docs/zeromq.md)
 * [Container Runtime integration](docs/cri.md)

## Architecture

Based on Promise Theory. designed to be control-plane-less. All nodes created equal. [info](docs/architecture.md)

## Community
Play nice with others please. [info](docs/community.md)

## Deployment Guide
[Here](docs/user_guide.md) is a best effort deployment guide.
