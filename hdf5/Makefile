include $(TOPDIR)/rules.mk

PKG_NAME:=hdf5
PKG_VERSION:=1.14.5
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/HDFGroup/hdf5/releases/download/hdf5_$(PKG_VERSION)/
PKG_HASH:=skip

PKG_MAINTAINER:=Esa Aprilia Salsabila <esaapriliasalsabila@gmail.com>
PKG_LICENSE:=License
PKG_LICENSE_FILES:=LICENSE LICENSE_LBNL_HDF5

PKG_BUILD_PARALLEL:=1

CMAKE_BINARY_SUBDIR := build

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/hdf5
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=HDF5 is a data model, library, and file format for storing and managing data
	DEPENDS:=+libaec +zlib +libstdcpp
	URL:=https://github.com/HDFGroup/hdf5/
endef

define Package/hdf5/description
	This repository contains a high-performance library's source code and a file format specification that implements the HDF5® data model.
	The model has been adopted across many industries, and this implementation has become a de facto data management standard in science, engineering, and research communities worldwide.
endef

CMAKE_OPTIONS += \
	-DBUILD_STATIC_LIBS=OFF \
	-DHDF5_BUILD_HL_LIB=ON \
	-DHDF5_BUILD_CPP_LIB=ON \
	-DHDF5_BUILD_FORTRAN=OFF \
	-DHDF5_BUILD_JAVA=OFF \
	-DHDF5_ENABLE_Z_LIB_SUPPORT=ON \
	-DHDF5_ENABLE_SZIP_SUPPORT=ON \
	-DHDF5_ENABLE_SZIP_ENCODING=ON \
	-DUSE_LIBAEC=ON

define Build/InstallDev
	$(INSTALL_DIR) \
	  $(1)/usr/include \
	  $(1)/usr/lib

	$(CP) \
	  $(PKG_INSTALL_DIR)/usr/include/* \
	  $(1)/usr/include/

	$(CP) \
	  $(PKG_INSTALL_DIR)/usr/lib/* \
	  $(1)/usr/lib/
	
	$(SED) \
	  's,/usr/include,$$$${prefix}/include,g' $(1)/usr/lib/pkgconfig/hdf5*.pc

	$(SED) \
	  's,/usr/lib,$$$${exec_prefix}/lib,g' $(1)/usr/lib/pkgconfig/hdf5*.pc

	$(SED) \
	  '/Requires/ s/-/ = /g' $(1)/usr/lib/pkgconfig/hdf5*.pc
endef

define Package/hdf5/install
	$(INSTALL_DIR) \
	  $(1)/usr/bin \
	  $(1)/usr/lib

	$(CP) \
	  $(PKG_INSTALL_DIR)/usr/bin/* \
	  $(1)/usr/bin/
	
	$(CP) \
	  $(PKG_INSTALL_DIR)/usr/lib/*.so* \
	  $(1)/usr/lib/
endef

$(eval $(call BuildPackage,hdf5))
