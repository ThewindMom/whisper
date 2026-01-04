# Contributing to Whisper

Thank you for your interest in contributing to Whisper! This document provides guidelines for contributing to the project.

## Development Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/openai/whisper.git
   cd whisper
   ```

2. Install ffmpeg (required dependency):
   ```bash
   # macOS
   brew install ffmpeg

   # Ubuntu/Debian
   sudo apt update && sudo apt install ffmpeg

   # Windows (Chocolatey)
   choco install ffmpeg
   ```

3. Install the package in development mode with test dependencies:
   ```bash
   pip install -e ".[dev]"
   ```

## Running Tests

Run the test suite with pytest:

```bash
pytest
```

For faster testing (skips large model tests):
```bash
pytest -k 'not test_transcribe or test_transcribe[tiny]'
```

## Code Style

- Follow PEP 8 guidelines
- Use type hints where appropriate
- Keep functions focused and well-documented

## Pull Request Process

1. Fork the repository and create a feature branch
2. Make your changes with clear, descriptive commits
3. Ensure all tests pass
4. Update documentation if needed
5. Submit a pull request against the `main` branch

## Reporting Issues

When reporting bugs, please include:
- Python and PyTorch versions
- Operating system
- Steps to reproduce the issue
- Error messages or unexpected behavior

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
