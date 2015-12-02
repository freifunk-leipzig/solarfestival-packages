#
# Copyright (C) 2013 Jo-Philipp Wich <jow@openwrt.org>
#
# Licensed under the Apache License, Version 2.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci2-freifunk-status-olsr
PKG_VERSION:=$(shell git --git-dir=$(CURDIR)/../.git log -1 --pretty="%ci %h" | awk '{ print $$1 "-" $$4 }')
PKG_MAINTAINER:=Ufo <ufo@rund.freifunk.net>


PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=


include $(INCLUDE_DIR)/package.mk


define Package/luci2-freifunk-status-olsr
  SECTION:=luci2
  CATEGORY:=LuCI2
  TITLE:=LuCI2 Status Freifunk OLSR
  DEPENDS:=
endef

define Package/luci2-freifunk-status-olsr/description
 Provides the LuCI2 module for freifunk status olsr page
endef


define Build/Configure
endef

define Build/Compile
endef


define Package/luci2-freifunk-status-olsr/install
	$(INSTALL_DIR) $(1)/www
	$(CP) ./htdocs/* $(1)/www/
endef


$(eval $(call BuildPackage,luci2-freifunk-status-olsr))
