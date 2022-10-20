# SPDX-License-Identifier: GPL-2.0

dtbo-$(CONFIG_MACH_A52SXQ_EUR_OPEN) += a52sxq_eur_open_w00_r02.dtbo
a52sxq_eur_open_w00_r02.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_A52SXQ_EUR_OPEN) += a52sxq_eur_open_w00_r01.dtbo
a52sxq_eur_open_w00_r01.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_A52SXQ_EUR_OPEN) += a52sxq_eur_open_w00_r00.dtbo
a52sxq_eur_open_w00_r00.dtbo-base := ../../../vendor/qcom/yupik.dtb

dtbo-$(CONFIG_MACH_A52SXQ_KOR_SINGLE) += a52sxq_kor_single_w00_r02.dtbo
a52sxq_kor_single_w00_r02.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_A52SXQ_KOR_SINGLE) += a52sxq_kor_single_w00_r01.dtbo
a52sxq_kor_single_w00_r01.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_A52SXQ_KOR_SINGLE) += a52sxq_kor_single_w00_r00.dtbo
a52sxq_kor_single_w00_r00.dtbo-base := ../../../vendor/qcom/yupik.dtb

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)

define __sec_dtbo_build
dtbo-$(2) += $(1)
$(1)-base := $(3)
endef

always          := $(dtb-y)
subdir-y        := $(dts-dirs)
endif

clean-files := *.dtb *.reverse.dts *.dtbo


