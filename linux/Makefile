
PROG = test

SRCS = main.c ../main/scpi-def.c
CFLAGS += -g -std=c99  -Wextra -Wmissing-prototypes -Wimplicit -I ../components/libscpi/inc/
LDFLAGS += -lm ../components/libscpi/dist/libscpi.a -Wl,--as-needed

.PHONY: clean all

all: $(PROG)

OBJS = $(SRCS:.c=.o)

.c.o:
	$(CC) -c $(CFLAGS) $(CPPFLAGS) -o $@ $<

$(PROG): $(OBJS)
	$(CC) -o $@ $(OBJS) $(CFLAGS) $(LDFLAGS)

clean:
	$(RM) $(PROG) $(OBJS)
