include $(TOPDIR)/rules.mk

ARCH:=arm
BOARD:=ipq40xx
BOARDNAME:=Qualcomm Atheros IPQ40XX
FEATURES:=squashfs fpu ramdisk nand
CPU_TYPE:=cortex-a7
CPU_SUBTYPE:=neon-vfpv4
MAINTAINER:=John Crispin <john@phrozen.org>
SUBTARGETS:=generic

# TODO: drop kmod-usb-dwc3-of-simple when migrating to 4.19
KERNEL_PATCHVER:=4.14

KERNELNAME:=zImage Image dtbs

include $(INCLUDE_DIR)/target.mk
DEFAULT_PACKAGES += \
	kmod-usb-dwc3-of-simple kmod-usb-dwc3-qcom \
	kmod-leds-gpio kmod-gpio-button-hotplug swconfig \
	kmod-ath10k wpad-openssl uboot-envtools \
	kmod-usb3 kmod-usb-dwc3 ath10k-firmware-qca4019 \
	autocore-arm e2fsprogs

$(eval $(call BuildTarget))
