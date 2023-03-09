# Copyright (C) 2023  Luke Shumaker <lukeshu@lukeshu.com>
#
# SPDX-License-Identifier: Apache-2.0

diff: binary-distribution-format.rst binary-distribution-format-go.rst
	diff --color=auto -u $^

binary-distribution-format.rst:
	curl https://raw.githubusercontent.com/pypa/packaging.python.org/main/source/specifications/binary-distribution-format.rst >$@

binary-distribution-format-go.rst: binary_distribution_format.go
	cat $< | sed -n -E 's,^	*//	> ?,,p' >$@
