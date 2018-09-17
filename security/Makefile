#
# Makefile for the kernel security code
#

obj-$(CONFIG_KEYS)			+= keys/
subdir-$(CONFIG_SECURITY_SELINUX)	+= selinux

subdir-$(CONFIG_ARCH_MSM)		+= pfe


# always enable default capabilities
obj-y					+= commoncap.o
obj-$(CONFIG_MMU)			+= min_addr.o

# Object file lists
ifeq ($(CONFIG_SECURITY_MIYABI),y)
obj-$(CONFIG_SECURITY)			+= security.o
else
obj-$(CONFIG_SECURITY)			+= security.o capability.o
endif
obj-$(CONFIG_SECURITYFS)		+= inode.o
obj-$(CONFIG_SECURITY_SELINUX)		+= selinux/
obj-$(CONFIG_SECURITY_SMACK)		+= smack/
obj-$(CONFIG_AUDIT)			+= lsm_audit.o


obj-$(CONFIG_ARCH_MSM)		        += pfe/
obj-$(CONFIG_CGROUP_DEVICE)		+= device_cgroup.o


# Object integrity file lists
subdir-$(CONFIG_INTEGRITY)		+= integrity
obj-$(CONFIG_INTEGRITY)			+= integrity/
