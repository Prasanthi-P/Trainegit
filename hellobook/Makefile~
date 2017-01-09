include $(TOPDIR)/rules.mk

PKG_NAME:=hellobook
PKG_VERSION:=1.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/hellobook
  SECTION:=utils 
  CATEGORY:=Utilities 
  TITLE:=hellobook

endef

define Package/hellobook/description
  Sample string operations
endef


define Build/Prepare 
	$(CP) src/* $(PKG_BUILD_DIR)/
endef

define Build/Compile
	$(MAKE) -C $(PKG_BUILD_DIR) $(MAKE_ARGS) all
endef

define Package/hellobook/install
	$(INSTALL_DIR) $(1)/bin 
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/hellobook $(1)/bin/ 
endef 

$(eval $(call BuildPackage,hellobook))
