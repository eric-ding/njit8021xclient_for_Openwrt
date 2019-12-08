# 
# Copyright (C) 2006-2008 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=njit8021xclient
PKG_RELEASE:=testing
PKG_VERSION:=1.4
PKG_SOURCE_URL:=https://github.com/eric-ding/njit8021xclient/releases/download/v$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_MD5SUM:=83b183b699efac3cbaf66b481008c69e
PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/njit8021xclient
  SECTION:=net
  CATEGORY:=Network
  TITLE:=NJIT 802.1X client program
  URL:=ttps://github.com/eric-ding/njit8021xclient
  DEPENDS:=+libpcap +libopenssl
endef

define Package/njit8021xclient/Default/description
 802.1X client from Nanjing Institude of Technology,
 compatable with H3C iNode 802.1X client.
 Support H3C/iNode's private authentication protocol V7.30-0505
endef

CONFIGURE_ARGS += \
	--program-prefix="njit-" \
	$(NULL)

define Build/Prepare
$(call Build/Prepare/Default)
endef

define Build/Configure
$(call Build/Configure/Default)
endef

define Package/njit8021xclient/install
	$(MAKE) -C $(PKG_BUILD_DIR) install-exec DESTDIR=$(1)
endef

define Package/njit8021xclient/conffiles
/etc/config/njit8021xclient.conf
endef

define Package/njit8021xclient/description
  $(call Package/njit8021xclient/Default/description)
  This package contains only the main program njit-client.
endef

$(eval $(call BuildPackage,njit8021xclient))
