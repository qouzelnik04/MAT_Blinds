# Software

## Introduction
- hardware has revision ([rev](../Schematic/README.md))
- software has version ([ver](./README.md))

For each software version, it is written which board revision it supports. This must be observed.
Each version of the software has detailed specifications of what it supports in the "README.md" file.

The software versions, their advantages and disadvantages are listed below.

## Actual version
### [ver_1.1](./ver_1.1/README.md) (not recommended)
- advantages
    - support 6 blinds
    - automatic pulling up and pulling down
- disadvantages
    - Required knowledge of STM32Cube to calibrate the blind.
    - support only Czech

### [ver_3.0](./ver_3.0/README.md) (recommended)
- advantages
    - easy to build (support [rev_3.0](../Schematic/rev_3.0/README.md))
    - support 4 blinds
    - automatic pulling up and pulling down
    - Supports English and Czech languages.

## Coming Soon
### [ver_2.0](./ver_2.0/README.md)
- advantages
    - Supports English and Czech languages.
    - support 6 blinds
    - automatic pulling up and pulling down
    - ...