PKG_NAME=wolfmqtt
PKG_URL=https://github.com/wolfssl/wolfMQTT.git
PKG_VERSION=0ba0929bfc0fbaffd5a612ed9c79eefcd0aea134 # v1.11.0
PKG_LICENSE=GPLv2

include $(RIOTBASE)/pkg/pkg.mk

# some variable seem uninitialized to gcc with -Og but are not
# https://gcc.gnu.org/bugzilla/buglist.cgi?quicksearch=may%20be%20used%20uninitialized
# https://gcc.gnu.org/bugzilla/show_bug.cgi?id=42145
# https://gcc.gnu.org/bugzilla/show_bug.cgi?id=90710#c1
CFLAGS += -Wno-maybe-uninitialized

all: #$(filter wolfmqtt,$(USEMODULE))
	$(QQ)"$(MAKE)" -C $(PKG_SOURCE_DIR)/src -f $(CURDIR)/Makefile.wolfmqtt

