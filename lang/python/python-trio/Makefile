#
# Copyright (C) 2022 Julien Malik <julien.malik@paraiso.me>
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python-trio
PKG_VERSION:=0.27.0
PKG_RELEASE:=1

PYPI_NAME:=trio
PKG_HASH:=1dcc95ab1726b2da054afea8fd761af74bad79bd52381b84eae408e983c76831

PKG_LICENSE:=Apache-2.0 MIT
PKG_LICENSE_FILES:=LICENSE.APACHE2 LICENSE.MIT
PKG_MAINTAINER:=Julien Malik <julien.malik@paraiso.me>

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

define Package/python3-trio
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Friendly library for async concurrency and I/O
  URL:=https://github.com/python-trio/trio
  DEPENDS:=+python3-light +python3-attrs +python3-sortedcontainers +python3-idna +python3-outcome +python3-sniffio +python3-cffi +python3-exceptiongroup
endef

define Package/python3-trio/description
The Trio project’s goal is to produce a production-quality, permissively
licensed, async/await-native I/O library for Python.
endef

$(eval $(call Py3Package,python3-trio))
$(eval $(call BuildPackage,python3-trio))
$(eval $(call BuildPackage,python3-trio-src))
