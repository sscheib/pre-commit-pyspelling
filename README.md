# `pre-commit-pyspelling`

This repository provides a [`pre-commit`](https://pre-commit.com/) hook for [`pyspelling`](https://github.com/facelessuser/pyspelling).

## Usage

To use it specify the following in your `.pre-commit-config.yaml`:

```yaml
  - repo: 'https://github.com/sscheib/pre-commit-pyspelling.git'
    rev: 'v1.0.0'
    hooks:
      - id: 'pyspelling'
```

If you want to pass filenames to `pyspelling`, you need to adjust the arguments:

```yaml
  - repo: 'https://github.com/sscheib/pre-commit-pyspelling.git'
    rev: 'v1.0.0'
    hooks:
      - id: 'pyspelling'
        pass_filenames: true
        args:
          - '--source'
```

Verbosity can be enabled via passing a command line argument as well:

```yaml
  - repo: 'https://github.com/sscheib/pre-commit-pyspelling.git'
    rev: 'v1.0.0'
    hooks:
      - id: 'pyspelling'
        verbose: true
        args:
          - '-vvv'
          - '--source'
```

## Documentation

Further configuration is possible. Please review the [`pre-commit`](https://pre-commit.com/) documentation, as well as the documentation for
[`pyspelling`](https://github.com/facelessuser/pyspelling).

## License

[`GPL-2.0-or-later`](LICENSE)
