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

# A52SXQ EUR
SEC_A52SXQ_EUR_DTBO := \
		a52sxq_eur_open_w00_r00.dtbo \
		a52sxq_eur_open_w00_r01.dtbo \
		a52sxq_eur_open_w00_r02.dtbo

# A52SXQ KOR
SEC_A52SXQ_KOR_DTBO := \
		a52sxq_kor_single_w00_r00.dtbo \
		a52sxq_kor_single_w00_r01.dtbo \
		a52sxq_kor_single_w00_r02.dtbo

# A52SXQ CHN
SEC_A52SXQ_CHN_DTBO := \
		a52sxq_chn_tw_w00_r00.dtbo \
		a52sxq_chn_tw_w00_r01.dtbo \
		a52sxq_chn_tw_w00_r02.dtbo

$(eval $(call sec_dtbo_build, \
		$(SEC_A52SXQ_EUR_DTBO),$(CONFIG_MACH_A52SXQ_EUR_OPEN),$(SEC_YUPIK_BASE_DTB)))

$(eval $(call sec_dtbo_build, \
		$(SEC_A52SXQ_KOR_DTBO),$(CONFIG_MACH_A52SXQ_KOR_SINGLE),$(SEC_YUPIK_BASE_DTB)))

$(eval $(call sec_dtbo_build, \
		$(SEC_A52SXQ_CHN_DTBO),$(CONFIG_MACH_A52SXQ_CHN_TW),$(SEC_YUPIK_BASE_DTB)))

always          := $(dtb-y)
subdir-y        := $(dts-dirs)
endif

clean-files := *.dtb *.reverse.dts *.dtbo
