# Samsung SDM450 Project

dtb-$(CONFIG_MACH_J8Y18LTE_CIS_SER) += sdm450-sec-j8y18lte_cis_ser-r00.dtb \
					sdm450-sec-j8y18lte_cis_ser-r01.dtb \
					sdm450-sec-j8y18lte_cis_ser-r02.dtb \
					sdm450-sec-j8y18lte_cis_ser-r03.dtb
					
dtb-$(CONFIG_MACH_J8Y18LTE_SWA_OPEN) += sdm450-sec-j8y18lte_swa_open-r00.dtb \
					sdm450-sec-j8y18lte_swa_open-r01.dtb \
					sdm450-sec-j8y18lte_swa_open-r02.dtb \
					sdm450-sec-j8y18lte_swa_open-r03.dtb
					
dtb-$(CONFIG_MACH_J8Y18LTE_SWA_INS) += sdm450-sec-j8y18lte_swa_ins-r00.dtb \
					sdm450-sec-j8y18lte_swa_ins-r01.dtb \
					sdm450-sec-j8y18lte_swa_ins-r02.dtb \
					sdm450-sec-j8y18lte_swa_ins-r03.dtb

dtb-$(CONFIG_MACH_J8Y18LTE_LTN_OPEN) += sdm450-sec-j8y18lte_ltn_open-r00.dtb \
					sdm450-sec-j8y18lte_ltn_open-r01.dtb \
					sdm450-sec-j8y18lte_ltn_open-r02.dtb \
					sdm450-sec-j8y18lte_ltn_open-r03.dtb
					
dtb-$(CONFIG_MACH_J8Y18LTE_MEA_JV) += sdm450-sec-j8y18lte_mea_jv-r00.dtb \
					sdm450-sec-j8y18lte_mea_jv-r01.dtb \
					sdm450-sec-j8y18lte_mea_jv-r02.dtb \
					sdm450-sec-j8y18lte_mea_jv-r03.dtb

dtb-$(CONFIG_MACH_J8Y18LTE_SEA_OPEN) += sdm450-sec-j8y18lte_sea_open-r00.dtb \
					sdm450-sec-j8y18lte_sea_open-r01.dtb \
					sdm450-sec-j8y18lte_sea_open-r02.dtb \
					sdm450-sec-j8y18lte_sea_open-r03.dtb

ifeq ($(CONFIG_ARM64),y)
always          := $(dtb-y)
subdir-y        := $(dts-dirs)
else
targets += dtbs
targets += $(addprefix ../, $(dtb-y))

$(obj)/../../%.dtb: $(src)/%.dts FORCE
        $(call if_changed_dep,dtc)

dtbs: $(addprefix $(obj)/../../,$(dtb-y))
endif
clean-files := *.dtb *.reserve.dts
