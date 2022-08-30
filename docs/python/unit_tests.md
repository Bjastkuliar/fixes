---
author: ''
category: Python
date: '2017-02-16'
summary: ''
title: Unit Tests
---
# Python Unit Tests

Included in python standard library

Test case - class that contains tests and other methods

Test methods must start with the name `test`

    import unittest
    import moves

    class MoveTests(unittest.TestCase)
      def test_five_plus_five(self):
        assert 5 + 5 == 10

      def test_one_plus_one(self):
        assert not 1 + 1 == 3


### Running a unit test

`python -m unittest tests.py`

### Make tests run without needing to specify module

Add to the bottom of the file:

    if __name__ == '__main__':
      unittest.main()

It checks if we run the file directly then run with unittest

### Structuring your tests

If your folder `tests/` and `module/` is in a `package/` folder. Then you can `cd package/` and run:

  python -m unittest discover -s tests/



### Running Tests with Setup.py

