# SPDX-License-Identifier: GPL-2.0

dtbo-$(CONFIG_MACH_M52XQ_EUR_OPEN) += m52xq_eur_open_w00_r05.dtbo
m52xq_eur_open_w00_r05.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_EUR_OPEN) += m52xq_eur_open_w00_r03.dtbo
m52xq_eur_open_w00_r03.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_EUR_OPEN) += m52xq_eur_open_w00_r02.dtbo
m52xq_eur_open_w00_r02.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_EUR_OPEN) += m52xq_eur_open_w00_r01.dtbo
m52xq_eur_open_w00_r01.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_EUR_OPEN) += m52xq_eur_open_w00_r00.dtbo
m52xq_eur_open_w00_r00.dtbo-base := ../../../vendor/qcom/yupik.dtb

dtbo-$(CONFIG_MACH_M52XQ_SWA_INS) += m52xq_swa_ins_w00_r05.dtbo
m52xq_swa_ins_w00_r05.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_SWA_INS) += m52xq_swa_ins_w00_r03.dtbo
m52xq_swa_ins_w00_r03.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_SWA_INS) += m52xq_swa_ins_w00_r02.dtbo
m52xq_swa_ins_w00_r02.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_SWA_INS) += m52xq_swa_ins_w00_r01.dtbo
m52xq_swa_ins_w00_r01.dtbo-base := ../../../vendor/qcom/yupik.dtb
dtbo-$(CONFIG_MACH_M52XQ_SWA_INS) += m52xq_swa_ins_w00_r00.dtbo
m52xq_swa_ins_w00_r00.dtbo-base := ../../../vendor/qcom/yupik.dtb

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)

define __sec_dtbo_build
dtbo-$(2) += $(1)
$(1)-base := $(3)
endef

define sec_dtbo_build
$(foreach dtbo, $(1), $(eval $(call __sec_dtbo_build, $(dtbo),$(2),$(3))))
endef

# YUPIK BASE DTB
SEC_YUPIK_BASE_DTB := ../../../vendor/qcom/yupik.dtb

always          := $(dtb-y)
subdir-y        := $(dts-dirs)
endif

clean-files := *.dtb *.reverse.dts *.dtbo


