# Nexora

**Nexora** is a lightweight, dependency-free repository intelligence CLI built with Python.

It analyzes a software project and provides a clear overview of its structure, codebase size, programming languages, largest files, empty files, and directory distribution.

No external packages are required.

## Features

* 📊 Language statistics
* 📁 Repository structure analysis
* 🧮 Total file and line counting
* 📦 Largest files detection
* 🔍 Empty file detection
* 🚫 Configurable ignored directories
* 🤖 JSON output for CI/CD workflows
* ⚡ Fast and dependency-free
* 🐍 Python standard library only

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/nexora.git
cd nexora
```

No dependencies are required.

## Usage

Analyze the current repository:

```bash
python nexora.py .
```

Analyze another project:

```bash
python nexora.py /path/to/project
```

Show the 20 largest files:

```bash
python nexora.py . --top 20
```

Export machine-readable JSON:

```bash
python nexora.py . --json
```

Ignore additional directories:

```bash
python nexora.py . --ignore cache temporary
```

## Example

```text
================================================================
  NEXORA — Repository Intelligence
================================================================

Repository : my-project
Files      : 184
Lines      : 27,491
Binary     : 12 skipped

Language Breakdown
----------------------------------------------------------------
Python                     72 files      18,421 lines
JavaScript                 41 files       5,293 lines
TypeScript                 29 files       2,981 lines
HTML                       18 files         521 lines
CSS                         9 files         275 lines
Other                      15 files           0 lines

Largest Files
----------------------------------------------------------------
src/core/engine.py                      84.2 KB     2,431 lines
src/api/server.py                       51.7 KB     1,382 lines
src/utils/parser.py                     38.4 KB       941 lines

================================================================
  Analysis complete.
================================================================
```

## JSON Output

Nexora can generate structured output suitable for automation:

```bash
python nexora.py . --json > report.json
```

This makes it easy to integrate Nexora into CI/CD pipelines, dashboards, quality checks, or internal developer tooling.

## Design Philosophy

Nexora intentionally uses only Python's standard library.

The goal is simple:

> Give developers useful repository intelligence without adding another dependency to the project.

## Roadmap

* [ ] Git history analysis
* [ ] Code complexity estimation
* [ ] Duplicate file detection
* [ ] Dependency analysis
* [ ] Markdown report generation
* [ ] CI/CD quality thresholds
* [ ] Interactive terminal dashboard
* [ ] Plugin architecture

## License

MIT License

Copyright (c) 2026 Nexora Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files, to deal in the Software
without restriction, including without limitation the rights to use, copy,
modify, merge, publish, distribute, sublicense, and/or sell copies of the
Software.
