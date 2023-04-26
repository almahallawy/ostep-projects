# specify all source files here
SRCS = kv.c
# specify target here (name of executable)
TARG = kv
# specify compiler, compile flags, and needed libs
CC = gcc
OPTS = -Wall -g 
LIBS = 
FLAG32 = -m32
FLAG64= -m64

# this translates .c files in src list to .o’s
OBJS = $(SRCS:.c=.o)

# all is not really needed, but is used to generate the target
all: $(TARG)

# this generates the target executable
$(TARG): $(SRCS)
	$(CC) $(FLAG32) -o $(TARG) $(SRCS) $(LIBS) 

# this is a generic rule for .o files
%.o: %.c
	$(CC) $(OPTS) -c $< -o $@
# and finally, a clean line

clean:
	rm -f $(OBJS) $(TARG) *~
