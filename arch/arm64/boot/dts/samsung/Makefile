# SPDX-License-Identifier: GPL-2.0

ifeq ($(filter y,$(CONFIG_SEC_A52SXQ_PROJECT)),y)
dts-dirs += a52/a52sxq
else ifeq ($(filter y,$(CONFIG_SEC_M52XQ_PROJECT)),y)
dts-dirs += m52/m52xq
endif

always          := $(dtb-y)
subdir-y        := $(dts-dirs)

clean-files := *.dtb *.reverse.dts *.dtbo
