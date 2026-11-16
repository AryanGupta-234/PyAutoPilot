# PyAutoPilot

A small Python module that scans the script importing it and installs any missing packages with pip.

## What it does

- Reads the running script (`sys.argv[0]`) and parses it with `ast` to find every `import` and `from ... import`.
- Compares those module names with the modules installed in the current environment.
- Runs `pip install` for each missing one, using the same Python interpreter.
- Maps known name differences, currently `win32com.client` to the `pywin32` package.
- Prints a dump of the parsed syntax tree while it runs (useful for debugging, noisy otherwise).

## Built with

- Python 3 standard library: `ast`, `pkgutil`, `subprocess`

## Run it

Install from PyPI:

    pip install PyAutoPilot

Or copy `PyAutoPilot.py` next to your script. Then import it at the top of your script, before your other imports:

    import PyAutoPilot

The check runs as soon as the module is imported.

## Security note

Installing packages executes third-party installation code. The module installs whatever names your imports use, and a module name does not always match the package that provides it. Review dependency names before relying on it, and use a virtual environment rather than a system-wide Python.

## Project status

Early learning project (version 0.1.0 on PyPI).

## License

MIT. See [LICENSE](LICENSE).

---

Part of [Aryan Gupta's projects](https://github.com/AryanGupta-234). Building [NOBAD](https://nobad-platform.aassworld99.workers.dev/): software with a point of view.
