export VENDOR = cloudposse
export PACKAGE_NAME = atmos
export PACKAGE_REPO_NAME = atmos
export DOWNLOAD_URL = $(PACKAGE_REPO_URL)/releases/download/$(PACKAGE_VERSION)/$(PACKAGE_NAME)_$(PACKAGE_VERSION)_$(OS)_$(ARCH)

## APK build specific requirements
export APK_BUILD_TEMPLATE = APKBUILD.github-binary
export APKBUILD_DEPENDS += libc6-compat

include ../../tasks/Makefile.vendor_includes

install:
	$(call download_binary)

test:
	printf 'TESTING binary by executing >>>: %s\n' '$(PACKAGE_EXE) version | grep -F $(PACKAGE_VERSION)'
	$(PACKAGE_EXE) version | grep -F $(PACKAGE_VERSION)
