CONTIKI_PROJECT = border-router
all: $(CONTIKI_PROJECT)
CONTIKI = ../..

# The BR is either native or embedded, and in the latter case must support SLIP
PLATFORMS_EXCLUDE = nrf52dk z1

# Include Multicast
MODULES += os/net/ipv6/multicast
MAKE_ROUTING = MAKE_ROUTING_RPL_CLASSIC

MAKE_MAC = MAKE_MAC_TSCH


# Activate orchestra
MODULES += os/services/orchestra



# Include RPL BR module
MODULES += os/services/rpl-border-router
# Include webserver module
MODULES_REL += webserver
# Include optional target-specific module
include $(CONTIKI)/Makefile.identify-target
MODULES_REL += $(TARGET)

include $(CONTIKI)/Makefile.include
