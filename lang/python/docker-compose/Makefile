include $(TOPDIR)/rules.mk

PKG_NAME:=docker-compose
PKG_VERSION:=1.26.0
PKG_RELEASE:=1

PYPI_NAME:=docker-compose
PKG_HASH:=7e836102d139aca667d6af53f0f4d942c9459ec24d6dd4f0203d74359b0fd311

PKG_MAINTAINER:=Javier Marcet <javier@marcet.info>
PKG_LICENSE:=Apache-2.0
PKG_LICENSE_FILES:=LICENSE

include ../pypi.mk
include $(INCLUDE_DIR)/package.mk
include ../python3-package.mk

PKG_USE_MIPS16:=0

PYTHON3_PKG_SETUP_ARGS:=

define Package/docker-compose
  SECTION:=lang
  CATEGORY:=Languages
  SUBMENU:=Python
  TITLE:=Docker Compose
  URL:=https://github.com/docker/compose
  DEPENDS+=+docker-ce \
      +python3 \
      +python3-cached-property \
      +python3-colorama \
      +python3-distro \
      +python3-distutils \
      +python3-docopt \
      +python3-docker \
      +python3-dockerpty \
      +python3-dotenv \
      +python3-jsonschema \
      +python3-pkg-resources \
      +python3-requests \
      +python3-setuptools \
      +python3-six \
      +python3-texttable \
      +python3-websocket-client \
      +python3-yaml
  VARIANT:=python3
endef

define Package/docker-compose/description
  Multi-container orchestration for Docker
endef

$(eval $(call Py3Package,docker-compose))
$(eval $(call BuildPackage,docker-compose))
$(eval $(call BuildPackage,docker-compose-src))
