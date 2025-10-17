![Template Banner](assets/template_banner.png)

# Python Template

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CI](https://github.com/tctibbs/template_python/actions/workflows/ci.yml/badge.svg)](https://github.com/tctibbs/template_python/actions/workflows/ci.yml)

A modern Python project template with automated development workflows and quality tools.

## Features

- **Modern Build System**: Uses `hatchling` with `uv` for fast dependency management
- **Code Quality**: Integrated linting and formatting with Ruff
- **Automation**: Makefile commands for common development tasks
- **Pre-commit Hooks**: Automated code quality checks before each commit
- **Production Docker**: Multi-stage Dockerfile optimized for security and size
- **DevContainer Support**: Ready-to-use development environment with Docker and VSCode

---

## Quick Start

### Prerequisites
- Python 3.11+
- [`uv`](https://docs.astral.sh/uv/getting-started/installation/) - Fast Python package installer

### Setup
```bash
git clone <your-repo-url>
cd template_python
make install
```

### Development Commands
```bash
make help     # Show all available commands
make lint     # Run linting and static analysis  
make format   # Format code and fix issues
make test     # Run test suite
make clean    # Remove build artifacts
```

---

## Docker Support

Build and run the project in a production-ready container:

```bash
# Build the image
docker build --tag template_python .

# Run Python REPL
docker run --rm -it template_python

# Execute Python code
docker run --rm template_python python -c "from python_template import add; print(add(2, 3))"

# Run with volume mounting for development
docker run --rm -v $(pwd):/app template_python python your_script.py
```

The production Dockerfile uses:
- Multi-stage build for minimal image size (~150MB)
- Non-root user for security
- Locked dependencies for reproducibility
- Python 3.13 slim base image

---

## Documentation

For detailed development setup, project structure, and contribution guidelines, see [DEVELOPMENT.md](DEVELOPMENT.md).
