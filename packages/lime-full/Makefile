#
# Copyright (C) 2013-2016 LibreMesh.org
#
# This is free software, licensed under the GNU General Public License v3.
#

include $(TOPDIR)/rules.mk

LIME_BUILDDATE:=$(shell date +%Y%m%d_%H%M)
LIME_CODENAME:=biggestbang

GIT_COMMIT_DATE:=$(shell git log -n 1 --pretty=%ad --date=short . )
GIT_COMMIT_TSTAMP:=$(shell git log -n 1 --pretty=%at . )

PKG_NAME:=lime-full
PKG_VERSION=$(GIT_COMMIT_DATE)-$(GIT_COMMIT_TSTAMP)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  TITLE:=libremesh standard metapackage
  SECTION:=lime
  CATEGORY:=LiMe
  SUBMENU:=Collections
  MAINTAINER:=Pau Escrich <p4u@dabax.net>
  URL:=http://libremesh.org
  DEPENDS:=+lime-basic +lime-debug +luci-mod-admin-full +lime-map-agent +lime-docs
endef

define Package/$(PKG_NAME)/description
	Metapackage depending on all the required to run a full standard libremesh node
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
