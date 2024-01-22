#
# Copyright (C) 2012-2015 OpenWrt.org
# Copyright (C) 2016 LEDE-Project.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=dosfstools
PKG_CPE_ID:=cpe:/a:dosfstools_project:dosfstools
PKG_VERSION:=4.3

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/hayzamjs/dosfstools/releases/download/$(PKG_VERSION)/
PKG_HASH:=9234c94acb09e075bee7ff85e95c40e4d039c4648e04a143601d9f1ea65bc1ec

HOST_FIXUP:=autoreconf

include $(INCLUDE_DIR)/host-build.mk

ifeq ($(HOST_OS),Darwin)
HOST_CFLAGS += -UHAVE_ENDIAN_H
endif

define Host/Uninstall
	-$(call Host/Compile/Default,uninstall)
endef

$(eval $(call HostBuild))
