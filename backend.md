# Backend

## Entity-Relationship Diagrams [ERD]

All ```boxcar``` projects include the following gem:

```
https://github.com/voormedia/rails-erd
```

The gem is installed and set to auto-update a file named ```ER_Model.pdf``` after each migration.
This file is linked to in the ```README.md``` for documentation purposes.

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
<<<<<<< HEAD
```
=======
```
>>>>>>> c95fd600b839fb556cb793de912278ab9d5ffe85
