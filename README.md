<!--
https://pypi.org/project/readme-generator/
https://pypi.org/project/python-readme-generator/
-->

#### Usage
```bash
curl -fLs https://run-tests.github.io/ | bash -s
```

#### Benefits
+   **native**. no need install anything
+   **all languages are supported**

#### How it works
+   files with [shebang](https://en.wikipedia.org/wiki/Shebang_(Unix)) (scripts) are executed
+   hidden folders and hidden scripts are ignored
+   tests failed if script exited with non-zero status

#### Examples
```
.
├── tests
│   ├── .include.py   # ignored
│   ├── example.py    # executed
│   └── example.sh    # executed
└── .travis.yml
```

`.travis.yml`
```xml
...
script: curl -fLs https://run-tests.github.io/ | bash -s
```

#### Pull Requests
pull requests are welcome :)

<p align="center">
    <a href="https://pypi.org/project/python-readme-generator/">python-readme-generator</a>
</p>