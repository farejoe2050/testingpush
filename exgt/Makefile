#this is done after comming back from feature3
#this is done for testing chnages made in branch
ifndef PETALINUX
$(error "Error: PETALINUX environment variable not set.  Change to the root of your PetaLinux install, and source the settings.sh file")
endif
#this is added to test changes after first time of code push
include apps.common.mk

all: build install

build: feature3 testing line

clean:

.PHONY: install image testing branch

install:
	$(TARGETINST) -d -p 0755 force_usb_power.sh /etc/init.d/force_usb_power.sh
	$(TARGETINST) -s /etc/init.d/force_usb_power.sh /etc/rc5.d/S99force_usb_power

help:
	@echo ""
	@echo "Quick reference for various supported build targets for $(INSTANCE)."
	@echo "----------------------------------------------------"
	@echo "  all                    build $(INSTANCE) and install to rootfs host copy"
	@echo "  install                install built objects to rootfs host copy"
