# SPDX-License-Identifier: GPL-2.0

ifeq ($(filter y,$(CONFIG_SEC_A52SXQ_PROJECT)),y)
dts-dirs += a52/a52sxq
endif

always          := $(dtb-y)
subdir-y        := $(dts-dirs)

clean-files := *.dtb *.reverse.dts *.dtbo
