# stanford-karel
[![Python 3.6+](https://img.shields.io/badge/python-3.6+-blue.svg)](https://www.python.org/downloads/release/python-360/)
[![PyPI version](https://badge.fury.io/py/stanfordkarel.svg)](https://badge.fury.io/py/stanfordkarel)
[![GitHub license](https://img.shields.io/github/license/TylerYep/stanford-karel)](https://github.com/TylerYep/stanford-karel/blob/master/LICENSE)
[![Downloads](https://pepy.tech/badge/stanfordkarel)](https://pepy.tech/project/stanfordkarel)

This is a Python implementation of Karel for Stanford's CS 106A. This package is available on PyPI and allows you to run Karel programs without any additional setup!

Huge thank you to @nickbowman for rewriting this project from scratch!


**StanfordKarel now supports:**
- Pip-installable package means you can run Karel programs from anywhere.
- Solution code no longer needed to grade assignments. Instead, the output world is compared.
- Karel in Ascii!
- Improved autograding, testing, linting, and auto-formatting.


# Usage
`pip install stanfordkarel`

or

`git clone https://github.com/tyleryep/stanfordkarel.git`


# Documentation
## Running Karel
First, ensure that Karel is correctly installed using pip.
If so, then any `.py` file can become a Karel program!

```python
from stanfordkarel import *


def main():
    """ Karel code goes here! """
    turnLeft()
    move()
    turnLeft()


if __name__ == "__main__":
    run_karel_program()
```

To run a specific problem, ensure that the Python file name and the world file name matches exactly.

### Folder structure
- `assignment1/`
    - `worlds/` (additional worlds go here)
        - `collect_newspaper_karel.w`
        - `collect_newspaper_karel_end.w`
    - `collect_newspaper_karel.py`


## Creating Worlds
If using the pip-installed version, simply run `python -m stanfordkarel.world_editor`.

To run the World Editor from the repository, simply run `python world_editor.py`.

## Grading
`./autograde` runs the available tests using pytest in the `tests/` folder and prints out any output differences in the world.
The tests use the student's code and the expected world output to determine correctness. If the output is not the same, the test driver will print out an ASCII representation of the differences.

![Autograder](./autograder.png)


## Development
Everything important is located in stanfordkarel/.


## Future Milestones
In the future, I hope to add:
- Automatic style checking
- Ways of determining the student's strategy or approach from observing Karel movements
- Autograde more worlds, broken down by assignment
- Allow students to autograde their own work
- Accessibility for visually-impaired students (using ascii karel)
