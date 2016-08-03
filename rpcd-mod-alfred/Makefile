#
# Copyright (C) 2013 Jo-Philipp Wich <jow@openwrt.org>
#
# Licensed under the Apache License, Version 2.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=rpcd-mod-alfred
PKG_VERSION:=$(shell git --git-dir=$(CURDIR)/../.git log -1 --pretty="%ci %h" | awk '{ print $$1 "-" $$4 }')
PKG_MAINTAINER:=Ufo <ufo@rund.freifunk.net>


PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=


include $(INCLUDE_DIR)/package.mk


define Package/rpcd-mod-alfred
  SECTION:=utils
  CATEGORY:=Base system
  TITLE:=OpenWrt ubus RPC backend server (alfred plugin)
  DEPENDS:=+rpcd +alfred-json
endef

define Package/rpcd-mod-alfred/description
 Provides the rpcd via ubus for alfred data types used in batman-adv mesh
endef


define Build/Configure
endef

define Build/Compile
endef


define Package/rpcd-mod-alfred/install
	$(INSTALL_DIR) $(1)
	$(CP) ./rpcd/* $(1)/
endef

$(eval $(call BuildPackage,rpcd-mod-alfred))
