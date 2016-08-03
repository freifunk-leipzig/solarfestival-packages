#
# Copyright (C) 2012-2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk
  
PKG_NAME:=alfred-json
PKG_VERSION:=0.3.1
PKG_RELEASE:=1
  
PKG_MAINTAINER:=Micha Stöcker <micha@freifunk-jena.de>
PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/ffnord/alfred-json/archive/
#PKG_SOURCE_URL:=https://github.com/ffnord/alfred-json/releases/download/$(PKG_VERSION)/
PKG_MD5SUM:=edd63102677b4354db547872c98e5995
  
include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk
  
CMAKE_INSTALL:=1
  
define Package/alfred-json
  SECTION:=net
  CATEGORY:=Network
  TITLE:=A.L.F.R.E.D - JSON Client
  URL:=https://github.com/ffnord/alfred-json
  DEPENDS:=jansson zlib
endef
  
CONFIGURE_ARGS+= LIBS="-Wl,-rpath-link=$(STAGING_DIR)/usr/lib"
  
define Package/alfred-json/description
 decompress gzipped alfred data
endef
  
define Package/alfred-json/install
        $(INSTALL_DIR) $(1)/usr/bin
        $(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/alfred-json $(1)/usr/bin/
endef
  
$(eval $(call HostBuild))
$(eval $(call BuildPackage,alfred-json))
#$(eval $(call BuildPackage,alfred-json,+jansson,+zlib))

