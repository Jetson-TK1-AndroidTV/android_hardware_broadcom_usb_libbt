# android_hardware_broadcom_usb_libbt

Generic Broadcom BCM USB Dongle Support

Some framework code requires this to enable BT
BOARD_HAVE_BLUETOOTH := true
BLUETOOTH_HCI_USE_USB := true
BOARD_HAVE_BLUETOOTH_BCM := true
BOARD_BLUETOOTH_BDROID_BUILDCFG_INCLUDE_DIR := device/brand/name/bluetooth

and for buildcfg

ifndef _BDROID_BUILDCFG_H
define _BDROID_BUILDCFG_H 
define BTM_DEF_LOCAL_NAME "Jetson TK1"
// At present either USB or UART is supporteddefine BLUETOOTH_HCI_USE_USB          TRUE
// Bluetooth Low Power Mode is supported on BT4.0
define HCILP_INCLUDED                 TRUE
endif
Also your kernel need UHID support.
