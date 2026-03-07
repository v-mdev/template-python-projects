# Template Python Projects

A comprehensive template repository for Python projects, designed to provide a solid foundation for developing, testing, and deploying Python applications.

## Features

- **Project Structure**: Well-organized directory layout following Python best practices
- **Testing Framework**: Pre-configured testing setup with pytest
- **Code Quality**: Integrated linting and formatting with Ruff and Mypy via pre-commit
- **Virtual Environment**: uv-based dependency management
- **CI/CD Ready**: GitHub Actions configuration templates
- **Development Tools**: Pre-commit hooks and development utilities

## After Cloning or Using as Template

Before starting development, make sure to apply the following changes:

1. **Rename the source folder**: `src/template-python-project/` → `src/<your-project-name>/`

2. **Update `pyproject.toml`**:
   - Change `name`, `version`, `description`, `authors`, and other metadata fields
   - Update the package source path to match your renamed `src/` folder

3. **Update pre-commit hook versions** in `.pre-commit-config.yaml` to the latest available:
   - Check [pre-commit-hooks releases](https://github.com/pre-commit/pre-commit-hooks/releases)
   - Check [ruff-pre-commit releases](https://github.com/astral-sh/ruff-pre-commit/releases)
   - Check [mirrors-mypy releases](https://github.com/pre-commit/mirrors-mypy/releases)
   - You can also check if the commented lines are useful for you.

4. **Install pre-commit hooks**:
```bash
uv run pre-commit install
```

5. **Configure GitHub Actions permissions**:
Go to your repository **Settings → Actions → General → Workflow permissions** and enable **"Allow GitHub Actions to create and approve pull requests"** if you want workflows to open PRs automatically.

## Quick Start

### Prerequisites

- Python 3.13 or higher
- [uv](https://docs.astral.sh/uv/) (for dependency management)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/v-mdev/template-python-projects.git
cd template-python-projects
```

2. Install dependencies:
```bash
uv sync
```

3. Install pre-commit hooks:
```bash
uv run pre-commit install
```

## Project Structure

```
template-python-projects/
├── src/                    # Source code (rename inner folder to your project name)
├── tests/                  # Test files
├── .github/                # GitHub workflows
├── pyproject.toml          # Project configuration (update with your project details)
├── .pre-commit-config.yaml # Pre-commit hooks (update hook versions)
├── README.md               # This file
└── .gitignore              # Git ignore rules
```

## Development

### Running Tests

```bash
uv run pytest
```

### Linting & Formatting

```bash
uv run ruff check --fix .
uv run ruff format .
```

### Type Checking

```bash
uv run mypy src/
```

### Run all pre-commit hooks manually

```bash
uv run pre-commit run --all-files
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
