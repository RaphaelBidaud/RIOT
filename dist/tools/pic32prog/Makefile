PKG_NAME     = pic32prog
PKG_URL      = https://github.com/sergev/pic32prog
PKG_VERSION  = b9f8db3b352804392b02b42475fc42874ac8bf04
PKG_LICENSE  = GPL-2
PKG_BUILDDIR = bin

# Building it requires some dependencies, on ubuntu:
#
#     sudo apt-get install libusb-dev libusb-1.0-0-dev libudev-dev

all: git-download
	@echo "[INFO] compiling pic32prog from source now"
	@env -i PATH=$(PATH) TERM=$(TERM) make -C $(PKG_BUILDDIR)
	@mv $(PKG_BUILDDIR)/pic32prog pic32prog

distclean::
	@rm -f pic32prog

include $(RIOTBASE)/pkg/pkg.mk
