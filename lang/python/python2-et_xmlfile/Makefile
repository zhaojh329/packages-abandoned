#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=python2-et_xmlfile
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

PKG_MAINTAINER:=Alexandru Ardelean <ardeleanalex@gmail.com>, Eneas U de Queiroz <cote2004-github@yahoo.com>
PKG_LICENSE:=MIT

PYPI_NAME:=et_xmlfile
PKG_HASH:=614d9722d572f6246302c4491846d2c393c199cfa4edc9af593437691683335b

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python2-package.mk

define Package/python-et_xmlfile/Default
  SUBMENU:=Python
  SECTION:=lang
  CATEGORY:=Languages
  TITLE:=Low memory library for creating large XML files.
  URL:=https://bitbucket.org/openpyxl/et_xmlfile
endef

define Package/python2-et_xmlfile
$(call Package/python-et_xmlfile/Default)
  DEPENDS:= \
	+PACKAGE_python2-et_xmlfile:python2-light \
	+PACKAGE_python2-et_xmlfile:python2-lxml
  VARIANT:=python2
endef

define Package/python2-et_xmlfile/description
  An implementation of lxml.xmlfile for the standard library.
  It is based upon the xmlfile module from lxml with the aim of
  allowing code to be developed that will work with both libraries.
endef

$(eval $(call Py2Package,python2-et_xmlfile))
$(eval $(call BuildPackage,python2-et_xmlfile))
$(eval $(call BuildPackage,python2-et_xmlfile-src))
