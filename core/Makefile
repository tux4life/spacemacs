## Makefile --- Spacemacs Core File
##
## Copyright (c) 2012-2014 Sylvain Benner
## Copyright (c) 2014-2015 Sylvain Benner & Contributors
##
## Author: Sylvain Benner <sylvain.benner@gmail.com>
## URL: https://github.com/syl20bnr/spacemacs
##
## This file is not part of GNU Emacs.
##
## License: GPLv3
EMACS_DIR=~/.emacs.d/
TEST_DIR=$(EMACS_DIR)core/tests/

all: test

test: unit_tests func_tests

unit_tests:
	@echo "-----------------------------------------------------------------"
	@echo "Unit Tests"
	@echo "-----------------------------------------------------------------"
	@emacs -batch -l ert                           \
    -l $(EMACS_DIR)core/load-paths.el            \
    -l $(TEST_DIR)configuration-layer-utest.el   \
    -f ert-run-tests-batch-and-exit

func_tests:
	@echo "-----------------------------------------------------------------"
	@echo "Functional Tests"
	@echo "-----------------------------------------------------------------"
	@emacs -batch -l ert                          \
    -l $(EMACS_DIR)core/load-paths.el           \
    -l $(TEST_DIR)spacemacs-mode-ftest.el       \
    -f ert-run-tests-batch-and-exit


.PHONY: test unit_tests func_tests
