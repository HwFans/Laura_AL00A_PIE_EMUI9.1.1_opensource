#never change compiling order(drivers initialization order) below
obj-$(CONFIG_HUAWEI_BATTERY_INFORMATION) += maxim/ nxp/ onewire/

ifneq ($(TARGET_BUILD_VARIANT),user)
ccflags-y += -DBATTERY_LIMIT_DEBUG
endif

ifeq ($(TARGET_VERSION_MODE),factory)
ccflags-y += -DBATTBD_FORCE_MATCH
endif

#this should be under maxim|nxp|onewire makefile obj-y
obj-$(CONFIG_HUAWEI_BATTERY_INFORMATION) += batt_info.o batt_aut_checker.o
