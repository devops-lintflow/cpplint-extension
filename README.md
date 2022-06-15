# cpplint-extension

[![Tag](https://img.shields.io/github/tag/devops-lintflow/cpplint-extension.svg?color=brightgreen)](https://github.com/devops-lintflow/cpplint-extension/tags)



## Introduction

*cpplint-extension* is an extension using the cpplint checker to provide C and C++ code style checker within
Visual Studio Code, forked from https://github.com/secularbird/cpplint-extension.



## Features

![feature](https://github.com/devops-lintflow/cpplint-extension/raw/main/feature.png)



## Requirements

```bash
git clone https://github.com/devops-lintflow/cpplint.git
cd cpplint
pip install -U pyinstaller
pyinstaller --clean --name cpplint -F cpplint.py
```



## Install

```bash
yarn
vsce package
vsce publish
```



## Settings

* `cpplint.cpplintPath`: set cpplint executable path, path on windows should like `C:\Users\github\devops-lintflow\cpplint\dist\cpplint.exe`
* `cpplint.lintMode`: set cpplint mode, avialable value are single and workspace
* `cpplint.lineLength`: set line length strict, default is 80 characters
* `cpplint.excludes`: set exclude rules, which is related path and shell globbing is preforming, abosluted path is supported right now,
  <pre>Examples:
  ["one.cc"]
  ["src/\*.cc"]
  ["src/\*.cc", "test/\*.cc"]</pre>
* `cpplint.filters`: set filters, only error messages whose category names pass the filters will be printed
* `cpplint.root`: set the root directory used for deriving header guard CPP variables
* `cpplint.repository`: set top level directory of the repository, used to derive the header guard CPP variable
* `cpplint.extensions`: set the allowed file extensions that cpplint will check
* `cpplint.languages`: set the allowed vscode language identifiers that cpplint will check *(Currently only on single file mode)*
* `cpplint.headers`: set the allowed header extensions that cpplint will consider to be header files
* `cpplint.verbose`: verbose level, errors with lower verbosity levels have lower confidence and are more likely to be false positives



## License

Project License can be found [here](LICENSE).



## Reference

- [publishing-extension](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
