# Installation
basically : git clone, mkvirtualenv <env> pip install -r requirements, make go :)

### Based on https://github.com/wizardofzos/flask-bootstrap-dev
It's a web-backend/frontend to demo the power of FSEQ2JSON :)

It has a receive-endpoint for the json push from the 'PERJSON'-job.
It will just receive the json, store it at "/static/jsons/perfdata.json" so the "/perfdata"-page can load in this
JSON via an AJAX-call to show the data in a tabular form.....

## HOWTO?
Just fire up the webapp, an naviate to http://localhost:5000/perfdata, then submit the job to se the auto-refresh happening :)

# Make file for lazy developer...

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

