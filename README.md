[![Actions Status](https://github.com/null-channel/legion/workflows/unit-tests/badge.svg)](https://github.com/null-channel/actions)
[![Actions Status](https://github.com/null-channel/legion/workflows/checks/badge.svg)](https://github.com/null-channel/actions)

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
   - [ ] container?
   - [ ] kube pod?
   - [ ] kube deployment?
   - [ ] kube service?
 - [ ] CP Storage
 - [ ] CP Consensus  
 - [ ] Machine taints
 - [ ] Network

## Youtube???
Yes, not only will I be streaming it a few nights a week on twitch starting later this year. I am going to make youtube videos covering the "how and whys" of the project. Because of this there are a few constraints this puts on the branching of the project. That being said, I would stay away from this project if I was you until at least 2023. And then watch the youtube series first and then join the live streams and THEN start contributing :)

#### Branching
There are 3 types of branches
 - Main - this is the main branch for development
 - vX.X - this is a release branch for the release of x.x
 - ytX - this is a branch that contains spesific code for youtube episode x

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
