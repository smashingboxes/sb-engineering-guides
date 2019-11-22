# Backend

## Entity-Relationship Diagrams [ERD]

All projects should include regularly updated ERD files at the README level.

Gem:
```
https://github.com/voormedia/rails-erd
```

Note: This gem ships with SB's Boxcar template.

## Python

### Best Practices

#### Imports

The file containing the `main()` function that starts the application should reside at the project's top-level folder so you can use "absolute" imports.

##### Example
```
project
├── main.py
├── package1
│   ├── module1.py
│   └── module2.py
└── package2
    ├── __init__.py
    ├── module3.py
    ├── module4.py
    └── subpackage1
        └── module5.py
```
Consider the above folder structure. If you start the app by running `python main.py` you can use the following "absolute" imports from any file.
```
from package1 import module1
from package1.module2 import function1
from package2.subpackage1.module5 import function2
```