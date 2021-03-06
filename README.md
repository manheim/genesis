genesis [![Build Status](https://travis-ci.org/bandwidthcom/genesis.svg?branch=master)](https://travis-ci.org/bandwidthcom/genesis)
=========

A Terraform CLI wrapper built by the Bandwidth Incubator.

#### Goals

1. Expose a command for each infrastructure-related lifecycle event in an Incubator-style project.
2. Each command should protect against accidental non-automated actions that impact infrastructure.
3. Don't do anything other than wrap the Terraform CLI
4. Be platform independent

Note: Still not tested on any OS other than Windows. Please submit an issue if there are problems!

This code base will be greatly simplified once Terraform allows for environment variable interpolation in ```tfvars``` files.

#### Installation

```gem install genesis```

#### Commands
- genesis apply
  - Apply infrastructure changes to match plan
- genesis destroy
  - Destroy infrastructure Terraform knows about
- genesis help [COMMAND]
  - Describe available commands or one specific command
- genesis plan
  - Output an execution plan
- genesis refresh
  - Reconcile state with the real-world infrastructure
- genesis show
  - Output contents of the state file

Note:
> All of these commands assume that the current working directory contains a ```terraform``` directory where terraform ```tf```, ```tf.json```, and ```tfvars``` files are. This is the directory passed to the Terraform cli.

#### Options
- [--prompt], [--no-prompt]
  - Prompt before executing dangerous commands (Default: true)


#### License
[MIT](LICENSE.txt)
