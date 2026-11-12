# PyAutoPilot

A Python utility that scans Python scripts for imports, checks whether corresponding packages are available, and can install missing dependencies.

## Features

- Import scanning
- Missing-dependency detection
- Module-to-package mapping for known naming differences
- Optional installation through pip

## Installation

    pip install PyAutoPilot

For a local source checkout, use the packaging configuration in this repository.

## Usage

    import PyAutoPilot

Refer to the package source and examples in this repository for supported invocation and configuration behavior.

## Security note

Installing packages executes third-party installation code. Review dependency names and package sources before enabling automatic installation. Use a virtual environment rather than a system-wide Python environment.

## Build

    python -m build

## License

See the repository's LICENSE file for applicable terms.
