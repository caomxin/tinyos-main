COMPONENT=EchoC

CFLAGS += -DCC2420_DEF_CHANNEL=$(TOS_CHANNEL)
CFLAGS += -DJN516_DEF_CHANNEL=$(TOS_CHANNEL)

# enable radio rx tx pins
CFLAGS += -DJN516_HWDEBUG_RADIO_RXTX_PINS

#blip2.0
PFLAGS += -DIN6_PREFIX=\"aaaa::\"
PFLAGS += -DLIB6LOWPAN_HC_VERSION=6

#rpl
PFLAGS += -DRPL_ROUTING -DRPL_STORING_MODE -I$(TINYOS_OS_DIR)/lib/net/rpl
PFLAGS += -DRPL_OF_0=1
PFLAGS += -DRPL_OF_MRHOF=0
PFLAGS += -DBLIP_SEND_ROUTER_SOLICITATIONS=1
PFLAGS += -DBLIP_SEND_ROUTER_ADVERTISEMENTS=1

#printf
#PFLAGS += -DNEW_PRINTF_SEMANTICS -DPRINTFUART_ENABLED
#CFLAGS += -I$(TINYOS_OS_DIR)/lib/printf

TINYOS_ROOT_DIR?=../../..

include $(TINYOS_ROOT_DIR)/Makefile.include

#make platform dependent ifdefs possible
#include $(TINYOS_ROOT_DIR)/support/make/util/target_platform.include
