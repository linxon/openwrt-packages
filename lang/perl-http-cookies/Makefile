#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=perl-http-cookies
PKG_VERSION:=6.07
PKG_RELEASE:=1

PKG_SOURCE:=HTTP-Cookies-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://cpan.metacpan.org/authors/id/O/OA/OALDERS
PKG_HASH:=6a2f8cde56074c9dc5b46a143975f19b981d0569f1d4dc5e80567d6aab3eea2a
PKG_BUILD_DIR:=$(BUILD_DIR)/perl/HTTP-Cookies-$(PKG_VERSION)

PKG_MAINTAINER:=Marcel Denia <naoir@gmx.net>
PKG_LICENSE:=GPL-1.0-or-later Artistic-1.0-Perl
PKG_LICENSE_FILES:=LICENSE

include $(INCLUDE_DIR)/package.mk
include ../perl/perlmod.mk

define Package/perl-http-cookies
  SUBMENU:=Perl
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=HTTP cookie jars
  URL:=https://search.cpan.org/dist/HTTP-Cookies/
  DEPENDS:=perl +perl-http-date +perl-http-message +perlbase-essential +perlbase-time
endef

define Build/Configure
        $(call perlmod/Configure,,)
endef

define Build/Compile
        $(call perlmod/Compile,,)
endef

define Package/perl-http-cookies/install
        $(call perlmod/Install,$(1),HTTP auto/HTTP)
endef


$(eval $(call BuildPackage,perl-http-cookies))
