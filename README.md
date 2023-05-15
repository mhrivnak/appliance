# OpenShift-based Appliance Builder

`openshift-appliance` is a command line utility for building a disk image that orchestrates OpenShift installation using the Agent-based installer. 

## Quick Start

Build and run: binary or container image

### Using the binary
* Install dependencies (libguestfs-tools/coreos-installer/oc)
* make build-appliance
* ./bin/openshift-appliance

#### Commands
* build
* clean
* generate-config

#### Flags
* --dir
* --log-level

### Using a container image

#### Configuration
``` bash
export IMAGE=<image_url>
export ASSETS=<assets_dir>
export LOG_LEVEL=info/debug/error
export CMD=build/clean/generate-config
```

#### Build and Run
make build run

## Development

### Running tests
```bash
skipper make test
```

### Running lint
```bash
make lint
```

## Main Components

### Recovery ISO Assets (pkg/asset/recovery/)
* BaseISO
* RecoveryISO

### Appliance Assets (pkg/asset/appliance/)
* BaseDiskImage
* ApplianceDiskImage

## High-Level Flow
