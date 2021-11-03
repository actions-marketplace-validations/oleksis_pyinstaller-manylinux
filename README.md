![Test](https://github.com/oleksis/pyinstaller-manylinux/workflows/Test/badge.svg)
# pyinstaller-manylinux
PyInstaller ManyLinux 2.24 Docker Action

This action run [PyInstaller](https://www.pyinstaller.org/) using docker image from [pypa/manylinux repository](https://quay.io/repository/pypa/manylinux_2_24_x86_64)

## Inputs

### `pyinstaller-params`

**Required** List of parameters for pyinstaller

## Example usage
```yaml
uses: oleksis/pyinstaller-manylinux@v2
with:
  pyinstaller-params: "['-c', '-F', '--icon=assets/image.ico', '--exclude-module=test', '--name=app-binary', 'app_module/__main__.py']"
```

See more in [test.yml](.github/workflows/test.yml)

## Notes

This action can execute **`setup.sh`** if it exists in the repository, before installing the requirements (**`requirements.txt`**)
