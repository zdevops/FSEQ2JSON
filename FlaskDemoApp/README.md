# Installation
basically : git clone, mkvirtualenv <env> pip install -r requirements, make go :)

### Based on https://github.com/wizardofzos/flask-bootstrap-dev
It's a web-backend/frontend to demo the power of FSEQ2JSON :)


Here's the Makefile stuff :

Runtime stuff:
  * run    Start the dev server at http://localhost:5000/
  * open   Open a browser to http://localhost:5000/
  * go     run && open at the same time

Development stuff:
  * rebuild-virtualenv
         Remove and rebuild the entire virtual Python environment
         and reinstalls all dependencies.
  * setup-deps
         Install dependencies in the current Python virtualenv.
  * clean  Throw away Python bytecode files, caches, and other junk
  * check  check Python syntax & coding style
  * test   run unit tests (verbose)
  * tt     run unit tests (compact)
  * t      same as tt, but fails fast

