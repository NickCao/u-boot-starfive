# SPDX-License-Identifier: GPL-2.0+

dtb-$(CONFIG_TARGET_AX25_AE350) += ae350_32.dtb ae350_64.dtb
dtb-$(CONFIG_TARGET_MICROCHIP_ICICLE) += microchip-mpfs-icicle-kit.dtb
dtb-$(CONFIG_TARGET_QEMU_VIRT) += qemu-virt32.dtb qemu-virt64.dtb
dtb-$(CONFIG_TARGET_OPENPITON_RISCV64) += openpiton-riscv64.dtb
dtb-$(CONFIG_TARGET_SIFIVE_UNLEASHED) += hifive-unleashed-a00.dtb
dtb-$(CONFIG_TARGET_SIFIVE_UNMATCHED) += hifive-unmatched-a00.dtb
dtb-$(CONFIG_TARGET_SIPEED_MAIX) += k210-maix-bit.dtb
ifeq ($(CONFIG_TARGET_STARFIVE_JH7100),y)
dtb-$(CONFIG_JH_EVB_V1) += starfive_jh7100_evb.dtb
dtb-$(CONFIG_JH_STARLIGHT) += starfive_jh7100_starlight.dtb
dtb-$(CONFIG_JH_STARLIGHT) += jh7100-beaglev-starlight.dtb
dtb-$(CONFIG_JH_STARLIGHT) += jh7100-beaglev-starlight-a1.dtb
dtb-$(CONFIG_JH_STARLIGHT) += jh7100-visionfive.dtb
endif

include $(srctree)/scripts/Makefile.dts

targets += $(dtb-y)

DTC_FLAGS += -R 4 -p 0x1000

PHONY += dtbs
dtbs: $(addprefix $(obj)/, $(dtb-y))
	@:

clean-files := *.dtb
