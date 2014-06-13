DEV_URL := "http://localhost:5000/"

all: help

help:
	@echo "Convenience Makefile for the lazy Developer"
	@echo
	@echo "Runtime stuff:"
	@echo "  run    Start the dev server at $(DEV_URL)"
	@echo "  open   Open a browser to $(DEV_URL)"
	@echo "  go     run && open at the same time"
	@echo
	@echo "Development stuff:"
	@echo "  rebuild-virtualenv"
	@echo "         Remove and rebuild the entire virtual Python environment"
	@echo "         and reinstalls all dependencies."
	@echo "  setup-deps"
	@echo "         Install dependencies in the current Python virtualenv."
	@echo "  clean  Throw away Python bytecode files, caches, and other junk"
	@echo "  check  check Python syntax & coding style"
	@echo "  test   run unit tests (verbose)"
	@echo "  tt     run unit tests (compact)"
	@echo "  t      same as tt, but fails fast"
	@echo

################
# Runtime stuff

run:
	foreman start

open:
	open $(DEV_URL)

go:
	(sleep 1; make open) &
	make run


####################
# Development stuff

setup-deps:
	pip install -r requirements.txt
	pip install -r dev-requirements.txt

clean:
	find . -name '*.pyc' -print0 | xargs -0 rm -r

check:
	@make check-syntax || true
	@make check-style || true

check-syntax:
	@find $(shell ls | egrep -v '(lib|bin|include)') -name '*.py' -print0 | xargs -0 pyflakes

check-style:
	@pep8 -r --exclude=lib,bin,include .

test:
	@python -m unittest discover -v -s tests

tt:
	@python -m unittest discover -s tests

t:
	@python -m unittest discover -s tests --failfast

