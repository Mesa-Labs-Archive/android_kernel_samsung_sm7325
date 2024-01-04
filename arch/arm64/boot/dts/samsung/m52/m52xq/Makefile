# SPDX-License-Identifier: GPL-2.0

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

# M52XQ EUR
SEC_M52XQ_EUR_DTBO := \
		m52xq_eur_open_w00_r00.dtbo \
		m52xq_eur_open_w00_r01.dtbo \
		m52xq_eur_open_w00_r02.dtbo \
		m52xq_eur_open_w00_r03.dtbo \
		m52xq_eur_open_w00_r05.dtbo

# M52XQ SWA
SEC_M52XQ_SWA_DTBO := \
		m52xq_swa_ins_w00_r00.dtbo \
		m52xq_swa_ins_w00_r01.dtbo \
		m52xq_swa_ins_w00_r02.dtbo \
		m52xq_swa_ins_w00_r03.dtbo \
		m52xq_swa_ins_w00_r05.dtbo

# M52XQ CIS
SEC_M52XQ_CIS_DTBO := \
		m52xq_cis_ser_w00_r00.dtbo \
		m52xq_cis_ser_w00_r01.dtbo \
		m52xq_cis_ser_w00_r02.dtbo \
		m52xq_cis_ser_w00_r03.dtbo \
		m52xq_cis_ser_w00_r05.dtbo

$(eval $(call sec_dtbo_build, \
		$(SEC_M52XQ_EUR_DTBO),$(CONFIG_MACH_M52XQ_EUR_OPEN),$(SEC_YUPIK_BASE_DTB)))

$(eval $(call sec_dtbo_build, \
		$(SEC_M52XQ_SWA_DTBO),$(CONFIG_MACH_M52XQ_SWA_INS),$(SEC_YUPIK_BASE_DTB)))

$(eval $(call sec_dtbo_build, \
		$(SEC_M52XQ_CIS_DTBO),$(CONFIG_MACH_M52XQ_CIS_SER),$(SEC_YUPIK_BASE_DTB)))

always          := $(dtb-y)
subdir-y        := $(dts-dirs)
endif

clean-files := *.dtb *.reverse.dts *.dtbo
