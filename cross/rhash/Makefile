PKG_NAME = RHash
PKG_VERS = 1.4.0
PKG_EXT = tar.gz
PKG_DIST_NAME = v$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = https://github.com/rhash/RHash/archive
PKG_DIST_FILE=$(PKG_NAME)-v$(PKG_VERS).$(PKG_EXT)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS =

HOMEPAGE = http://rhash.sourceforge.net/
COMMENT  = RHash (Recursive Hasher) is a console utility for computing and verifying hash sums of files. It supports CRC32, CRC32C, MD4, MD5, SHA1, SHA256, SHA512, SHA3, AICH, ED2K, DC++ TTH, BitTorrent BTIH, Tiger, GOST R 34.11-94, RIPEMD-160, HAS-160, EDON-R, and Whirlpool.
LICENSE  = MIT


ifeq ($(findstring $(ARCH), $(ARM5_ARCHES) $(ARM7_ARCHES)),$(ARCH))
CONFIGURE_ARGS = --target=arm-linux
endif
ifeq ($(findstring $(ARCH), $(ARM8_ARCHES)),$(ARCH))
CONFIGURE_ARGS = --target=aarch64-linux
endif
ifeq ($(findstring $(ARCH), $(PPC_ARCHES)),$(ARCH))
CONFIGURE_ARGS = --target=ppc-linux
endif
ifeq ($(findstring $(ARCH), $(x86_ARCHES)),$(ARCH))
CONFIGURE_ARGS = --target=x86-linux
endif
ifeq ($(findstring $(ARCH), $(x64_ARCHES)),$(ARCH))
CONFIGURE_ARGS = --target=x86_64-linux
endif
CONFIGURE_ARGS += --prefix=$(INSTALL_PREFIX) --enable-symlinks --enable-static

include ../../mk/spksrc.cross-cc.mk
