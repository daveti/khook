MODNAME		?= khook-demo

obj-m		+= $(MODNAME).o
$(MODNAME)-y	+= main.o

ccflags-y	+= -fno-stack-protector -fvisibility=hidden
ldflags-y	+= -T$(src)/engine/engine.lds

KBUILD_CFLAGS	:= $(filter-out -pg,$(KBUILD_CFLAGS))
KBUILD_CFLAGS	:= $(filter-out -mfentry,$(KBUILD_CFLAGS))
