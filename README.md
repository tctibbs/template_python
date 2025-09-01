![Template Banner](assets/template_banner.png)

# Python Template

A modern Python project template with automated development workflows and quality tools.

## Features

- **Modern Build System**: Uses `hatchling` with `uv` for fast dependency management
- **Code Quality**: Integrated linting, formatting, and type checking with Ruff and MyPy
- **Automation**: Makefile commands for common development tasks
- **Pre-commit Hooks**: Automated code quality checks before each commit
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
make lint     # Run linting and type checking  
make format   # Format code and fix issues
make test     # Run test suite
make clean    # Remove build artifacts
```

---

## Documentation

For detailed development setup, project structure, and contribution guidelines, see [DEVELOPMENT.md](DEVELOPMENT.md).

## License

This project is licensed under the MIT License. See the LICENSE file for details.
