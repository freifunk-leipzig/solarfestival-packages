#
# Copyright (C) 2013 Jo-Philipp Wich <jow@openwrt.org>
#
# Licensed under the Apache License, Version 2.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci2-rpcd-alfred
PKG_VERSION:=$(shell git --git-dir=$(CURDIR)/../.git log -1 --pretty="%ci %h" | awk '{ print $$1 "-" $$4 }')
PKG_MAINTAINER:=Ufo <ufo@rund.freifunk.net>


PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=


include $(INCLUDE_DIR)/package.mk


define Package/luci2-rpcd-alfred
  SECTION:=luci2
  CATEGORY:=LuCI2
  TITLE:=LuCI2 rpcd Alfred for batman-adv meshrouting
  DEPENDS:=+rpcd
endef

define Package/luci2-rpcd-alfred/description
 Provides the rpcd via ubus for alfred data types used in batman-adv mesh
endef


define Build/Configure
endef

define Build/Compile
endef


define Package/luci2-rpcd/install
	$(INSTALL_DIR) $(1)
	$(CP) ./rpcd/* $(1)/
endef

define Package/luci2-rpcd-alfred/postinst
#!/bin/sh

echo postinstall luci2-rpcd-alfred

exit 0
endef

$(eval $(call BuildPackage,luci2-rpcd-alfred))
