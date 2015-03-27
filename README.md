# Debian lx-brand Image Builder

This is a collection of scripts used for creating an lx-brand Debian image.

## Requirements

In order to use these scripts you'll need:

- Debian running in a VM or bare metal (required for the `install` script)
- debootstrap: `apt-get install -y debootstrap`
- A SmartOS (or SDC headnode) install (required for the `create-lx-image` script)

## Usage

1. Run ./install under Debian to install Debian 7 in a directory. This will create a tarball of the installation in your working directory (named `debian-7-lx-$YYMMDD.tar.gz`)
2. Copy the tarball to a SmartOS machine or SDC headnode and run `./create-lx-image -t debian-7-lx-$YYMMDD.tar.gz` (substituting the name of your tar file). This will create the image file and manifest.
