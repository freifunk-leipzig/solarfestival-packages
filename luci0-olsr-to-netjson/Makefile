#
# Copyright (C) 2015
#
# Licensed under the Apache License, Version 2.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci0-olsr-to-netjson
PKG_VERSION:=$(shell git --git-dir=$(CURDIR)/../.git log -1 --pretty="%ci %h" | awk '{ print $$1 "-" $$4 }')
PKG_MAINTAINER:=Ufo <ufo@rund.freifunk.net>


PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=


include $(INCLUDE_DIR)/package.mk


define Package/luci0-olsr-to-netjson
  SECTION:=luci2
  CATEGORY:=LuCI2
  TITLE:=LuCI0 OLSR to netJSON
endef

define Package/luci0-olsr-to-netjson/description
 Provides a webview for olsr networks via netjson
endef


define Build/Configure
endef

define Build/Compile
endef


define Package/luci0-olsr-to-netjson/install
	$(INSTALL_DIR) $(1)/www
	$(CP) ./htdocs/* $(1)/www/
	$(INSTALL_DIR) $(1)
	$(CP) ./files/* $(1)/
endef

define Package/luci0-olsr-to-netjson/postinst
#!/bin/sh

echo postinstall  luci0-olsr-to-netjson

exit 0
endef

$(eval $(call BuildPackage,luci0-olsr-to-netjson))
