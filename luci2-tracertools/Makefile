#
# Copyright (C) 2013 Jo-Philipp Wich <jow@openwrt.org>
#
# Licensed under the Apache License, Version 2.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci2-tracertools
PKG_VERSION:=$(shell git --git-dir=$(CURDIR)/../.git log -1 --pretty="%ci %h" | awk '{ print $$1 "-" $$4 }')
PKG_MAINTAINER:=Ufo <ufo@rund.freifunk.net>

PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Build/Prepare
endef

define Package/luci2-tracertools
  SECTION:=luci2
  CATEGORY:=LuCI2
  TITLE:=LuCI2 Tracertools
  DEPENDS:=+luci2
endef

define Package/luci2-tracertools/description
 Provides the LuCI2 module for Solar Charge Controllers
endef

define Package/luci2-tracertools/install
	$(INSTALL_DIR) $(1)/www
	$(CP) ./htdocs/* $(1)/www/
	$(INSTALL_DIR) $(1)/usr/share/rpcd
	$(CP) ./share/* $(1)/usr/share/rpcd/
endef

define Package/luci2-tracertools/postinst
#!/bin/sh

echo postinstall  tracertools

exit 0
endef

$(eval $(call BuildPackage,luci2-tracertools))
