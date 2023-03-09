# Copyright (C) 2023  Luke Shumaker <lukeshu@lukeshu.com>
#
# SPDX-License-Identifier: Apache-2.0

diff: pep-0440.rst pep-0440-go.rst
	diff --color=auto -u $^
.PHONY: diff

pep-0440.rst:
	curl https://raw.githubusercontent.com/python/peps/main/pep-0440.txt >$@

pep-0440-go.rst: $(wildcard *.go)
	cat $(sort $^) | sed -n -E 's,^	*//	> ?,,p' >$@
